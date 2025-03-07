# Test-K-BIT
Descripción del Proyecto
Este proyecto es una implementación de un sistema de evaluación basado en el Test K-BIT (Kaufman Brief Intelligence Test), diseñado para medir habilidades cognitivas en niños y adultos. El sistema está compuesto por tres subtests principales:

Subtest de Vocabulario Expresivo (Test A): Evalúa la capacidad del examinado para identificar y nombrar objetos a partir de imágenes.

Subtest de Vocabulario de Definiciones (Test B): Evalúa la comprensión y definición de palabras.

Subtest de Matrices: Evalúa el razonamiento no verbal mediante la resolución de problemas visuales.

El sistema está desarrollado en Python utilizando la biblioteca Tkinter para la interfaz gráfica y PIL (Pillow) para el manejo de imágenes. Los resultados se almacenan en un archivo JSON (resultados.json) para su posterior análisis.

Estructura del Proyecto
El proyecto está organizado en los siguientes módulos:

Pantalla Inicial: Recopila los datos del examinado (nombre, edad, sexo, etc.) y calcula la edad cronológica.

InterfazTestA: Implementa el Subtest de Vocabulario Expresivo.

InterfazTestB: Implementa el Subtest de Vocabulario de Definiciones.

InterfazSubtestMatrices: Implementa el Subtest de Matrices.

Configuraciones: Archivos de configuración para cada subtest, que definen las preguntas, respuestas correctas y rutas de las imágenes.

Requisitos
Python 3.7 o superior.

Bibliotecas necesarias:

tkinter (incluida en Python estándar).

Pillow (para manejo de imágenes): Instalar con pip install pillow.

json (incluida en Python estándar).

os y sys (incluidas en Python estándar).

Configuración
Cada subtest utiliza un archivo de configuración específico para definir las preguntas, respuestas correctas y rutas de las imágenes. A continuación, se describen los archivos de configuración:

1. Subtest de Matrices (configSubtestMatrices.py)
RESPUESTAS_MATRICES: Diccionario con las respuestas correctas para cada pregunta.

SECCIONES_MATRICES: Define las secciones del test y los rangos de preguntas.

IMAGENES_DIR: Ruta del directorio que contiene las imágenes para las preguntas.

2. Subtest de Vocabulario Expresivo (configTestA.py)
PREGUNTAS_SECCIONES: Lista de preguntas organizadas en secciones.

SECCION_INICIAL_POR_EDAD: Define la sección inicial según la edad del examinado.

IMAGENES_DIR: Ruta del directorio que contiene las imágenes para las preguntas.

3. Subtest de Vocabulario de Definiciones (configTestB.py)
RESPUESTAS_POR_SECCION: Diccionario con las respuestas correctas organizadas por secciones.

INICIO_POR_EDAD: Define la sección inicial según la edad del examinado.

IMAGENES_DIR: Ruta del directorio que contiene las imágenes para las preguntas.

Instrucciones de Uso
Ejecutar el programa:

Ejecuta el archivo PantallaInicial.py para iniciar la aplicación.

Ingresa los datos del examinado en el formulario y haz clic en "Iniciar Test".

Realizar los subtests:

El sistema guiará al examinado a través de los subtests correspondientes según su edad.

En cada pregunta, el examinado debe ingresar su respuesta y validarla.

Resultados:

Al finalizar cada subtest, se muestra un resumen de respuestas correctas e incorrectas.

Los resultados se guardan automáticamente en el archivo resultados.json.

Avanzar al siguiente test:

Después de completar un subtest, el sistema permite avanzar al siguiente o finalizar la evaluación.

Notas Adicionales
Imágenes: Asegúrate de que las imágenes estén en las rutas especificadas en los archivos de configuración.

Edad: El sistema está diseñado para examinados de 4 a 90 años. Si la edad está fuera de este rango, se mostrará un error.
