# RTSH
# Analizador de Requisitos de Trabajo con IA

Este proyecto utiliza el modelo de lenguaje Gemini Pro de Google para analizar ofertas de trabajo y extraer información clave de manera estructurada. Convierte texto de ofertas de trabajo en datos útiles para candidatos y reclutadores.

## Funcionalidades

1.  **Análisis Inteligente**: Utiliza Gemini Pro para identificar y extraer:
    *   Título del proyecto
    *   Objetivo principal
    *   Habilidades técnicas requeridas (con ponderación de importancia)
    *   Áreas de experiencia
    *   Alcance del proyecto
    *   Responsabilidades clave
    *   Requisitos técnicos y adicionales
    *   Detalles del proyecto (duración, modalidad, etc.)
    *   Industria/Dominio

2.  **Formato Estructurado**: Organiza la información extraída en un formato JSON claro y fácil de usar.

3.  **Ponderación de Habilidades**: Asigna un peso a las habilidades técnicas según su frecuencia y relevancia en la oferta, lo que ayuda a los candidatos a priorizar su aprendizaje.

4.  **Guardado de Resultados**: Permite guardar los análisis en archivos JSON para su posterior consulta o procesamiento.

## Cómo Funciona

1.  **Entrada**: Se proporciona el texto de una oferta de trabajo.

2.  **Procesamiento**:
    *   El código utiliza un _prompt_ para indicarle a Gemini Pro qué información extraer.
    *   La respuesta de Gemini se convierte a un formato estructurado.
    *   Se ponderan las habilidades técnicas.

3.  **Salida**: Se devuelve un diccionario de Python con el análisis estructurado, que puede ser guardado como JSON.

## Uso

### Requisitos

*   Python 3.6+
*   Bibliotecas: `google-generativeai`, `python-dotenv`
*   Clave de API de Gemini Pro (variable de entorno `GEMMA_API_KEY`)

### Instalación

`pip install google-generativeai python-dotenv`

# Analizador de Currículums (CV) con IA

Este proyecto utiliza el modelo de lenguaje Gemini Pro de Google para analizar currículums (CVs) en formato PDF y extraer información clave de manera estructurada.  Convierte el texto de un CV en datos útiles para reclutadores y candidatos.

## Funcionalidades

1.  **Extracción de Texto desde PDF**: Extrae el texto de archivos PDF, preprocesándolo para eliminar ruido y estandarizar formatos (emails, teléfonos).

2.  **Análisis Inteligente**: Utiliza Gemini Pro para identificar y extraer:
    *   Resumen Personal
    *   Habilidades Clave
    *   Experiencia Laboral (Empresa, Cargo, Fechas, Responsabilidades)
    *   Educación (Títulos, Certificaciones)
    *   Habilidades Técnicas
    *   Idiomas (con nivel de dominio)
    *   Logros

3.  **Formato Estructurado**: Organiza la información extraída en un diccionario de Python, que luego se puede guardar como JSON.

4.  **Generación de Resumen**: Crea un resumen profesional conciso del CV, destacando la experiencia, habilidades y logros más relevantes.

5.  **Guardado de Resultados**: Permite guardar el análisis detallado y el resumen en un archivo JSON para su posterior consulta o procesamiento.

## Cómo Funciona

1.  **Entrada**: Se proporciona la ruta a un archivo PDF de currículum.

2.  **Procesamiento**:
    *   El código extrae el texto del PDF y lo preprocesa.
    *   Se utiliza un _prompt_ para indicarle a Gemini Pro qué información extraer del texto del CV.
    *   La respuesta de Gemini se convierte a un formato estructurado (diccionario de Python).
    *   Se genera un resumen del CV utilizando Gemini Pro.

3.  **Salida**: Se devuelve un diccionario de Python con el análisis estructurado y el resumen, que se guarda como JSON.  También se imprime el resumen y el análisis por consola.

## Uso

### Requisitos

*   Python 3.6+
*   Bibliotecas: `PyPDF2`, `google-generativeai`, `python-dotenv`
*   Clave de API de Gemini Pro (variable de entorno `GEMMA_API_KEY`)

### Instalación

```bash
pip install PyPDF2 google-generativeai python-dotenv
