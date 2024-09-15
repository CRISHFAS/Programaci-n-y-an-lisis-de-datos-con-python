# Programación y Análisis de Datos con Python

## Resumen y Cronograma

La mejor manera de aprender a programar es hacer algo útil, por lo que esta introducción a Python está construida en torno a una tarea científica común: el análisis de datos.

### Escenario: Una cura milagrosa para la inflamación de la artritis

Nuestro colega imaginario, el Dr. Maverick, ha inventado un nuevo medicamento milagroso que promete curar los brotes de inflamación de la artritis después de solo 3 semanas desde que se tomó el medicamento por primera vez. Naturalmente, deseamos ver los datos del ensayo clínico y, después de meses de solicitarlos, finalmente nos han proporcionado una hoja de cálculo CSV que contiene los datos del ensayo clínico.

El archivo CSV contiene la cantidad de brotes de inflamación por día de los 60 pacientes que participaron en el ensayo clínico inicial, que duró 40 días. Cada fila corresponde a un paciente y cada columna corresponde a un día del ensayo. Una vez que un paciente tiene su primer brote de inflamación, toma el medicamento y espera unas semanas para que surta efecto y reduzca los brotes.

Para comprobar la eficacia del tratamiento nos gustaría:
- Calcular la inflamación promedio por día en todos los pacientes.
- Graficar el resultado para discutirlo y compartirlo con sus colegas.

El diagrama de flujo de tres pasos muestra los registros de datos de inflamación de los pacientes que pasan al paso de Análisis, donde se genera un mapa de calor de los datos proporcionados y pasa al paso de Conclusión que plantea la pregunta: ¿Cómo afecta la medicación a los pacientes?

## Formato de Datos

Los conjuntos de datos se almacenan en formato de valores separados por comas (CSV):
- Cada fila contiene información de un solo paciente,
- Las columnas representan días sucesivos.

Las primeras tres filas de nuestro primer archivo se ven así:

```plaintext
0,0,1,3,1,2,4,7,8,3,3,3,10,5,7,4,7,7,12,18,6,13,11,11,7,7,4,6,8,8,4,4,5,7,3,4,2,3,0,0
0,1,2,1,2,1,3,2,2,6,10,11,5,9,4,4,7,16,8,6,18,4,12,5,12,7,11,5,11,3,3,5,4,4,5,5,1,1,0,1
0,1,1,3,3,2,6,2,5,9,5,7,4,5,4,15,5,11,9,10,19,14,12,17,7,12,11,7,4,2,10,5,4,2,2,3,2,2,1,1
```

Cada número representa el número de episodios de inflamación que experimentó un paciente en particular en un día determinado.

Por ejemplo, el valor “6” en la fila 3, columna 7 del conjunto de datos anterior significa que el tercer paciente experimentó inflamación seis veces en el séptimo día del estudio clínico.

Para poder analizar estos datos e informar a nuestros colegas, tendremos que aprender un poco de programación.

## Prerrequisitos

Debe comprender los conceptos de archivos y directorios y cómo iniciar un intérprete de Python antes de abordar esta lección. Esta lección a veces hace referencia a Jupyter Notebook, aunque puede usar cualquier intérprete de Python mencionado en la configuración.

Los comandos de esta lección se aplican a cualquier versión de Python oficialmente compatible, actualmente Python 3.8+. Las versiones más nuevas suelen tener mejores impresiones de errores, por lo que se recomienda usar versiones más nuevas de Python si es posible.

## Empezando

Para comenzar, siga las instrucciones de la página de configuración para descargar datos e instalar un intérprete de Python.

### Instrucciones de Instalación

**Duración: 00h 00m**  
1. **Fundamentos de Python**  
   - ¿Con qué tipos de datos básicos puedo trabajar en Python? 
   - ¿Cómo puedo crear una nueva variable en Python? 
   - ¿Cómo uso una función?
   - ¿Puedo cambiar el valor asociado a una variable después de crearla?

**Duración: 00h 30m**  
2. **Análisis de los datos del paciente**  
   - ¿Cómo puedo procesar archivos de datos tabulares en Python?

**Duración: 01h 30m**  
3. **Visualización de datos tabulares**  
   - ¿Cómo puedo visualizar datos tabulares en Python? 
   - ¿Cómo puedo agrupar varios gráficos?

**Duración: 02h 20m**  
4. **Almacenamiento de múltiples valores en listas**  
   - ¿Cómo puedo almacenar muchos valores juntos?

**Duración: 03h 05m**  
5. **Repetición de acciones con bucles**  
   - ¿Cómo puedo realizar las mismas operaciones en muchos valores diferentes?

**Duración: 03h 35m**  
6. **Análisis de datos de varios archivos**  
   - ¿Cómo puedo realizar las mismas operaciones en muchos archivos diferentes?

**Duración: 03h 55m**  
7. **Tomar decisiones**  
   - ¿Cómo pueden mis programas hacer cosas diferentes según los valores de los datos?

**Duración: 04h 25m**  
8. **Creación de funciones**  
   - ¿Cómo puedo definir nuevas funciones?  
   - ¿Cuál es la diferencia entre definir y llamar a una función?  
   - ¿Qué sucede cuando llamo a una función?

**Duración: 04h 55m**  
9. **Errores y excepciones**  
   - ¿Cómo informa Python los errores?  
   - ¿Cómo puedo gestionar los errores en los programas Python?

**Duración: 05h 25m**  
10. **Programación defensiva**  
    - ¿Cómo puedo hacer que mis programas sean más confiables?

**Duración: 06h 05m**  
11. **Depuración**  
    - ¿Cómo puedo depurar mi programa?

## Descripción General

Esta lección está diseñada para ejecutarse en una computadora personal. Todo el software y los datos utilizados en esta lección están disponibles gratuitamente en línea y a continuación se proporcionan instrucciones sobre cómo obtenerlos.

### Instalar Python

En esta lección, utilizaremos Python 3 con algunas de sus bibliotecas científicas más populares. Aunque se puede instalar un Python básico y todas las bibliotecas necesarias a mano, recomendamos instalar [Anaconda](https://www.anaconda.com/products/distribution), una distribución de Python que viene con todo lo que necesitamos para la lección. Se pueden encontrar instrucciones de instalación detalladas para varios sistemas operativos en el [sitio web de Anaconda](https://docs.anaconda.com/anaconda/install/) y en la [documentación de The Carpentries](https://carpentries.org/workshops/).

### Obtener Materiales de Clase

1. Descargue `python-novice-inflammation-data.zip` y `python-novice-inflammation-code.zip`.
2. Crea una carpeta llamada `swc-python` en tu Escritorio.
3. Mueve los archivos descargados a `swc-python`.
4. Descomprima los archivos.
5. Deberías ver dos carpetas llamadas `data` y `code` en el directorio `swc-python` de tu escritorio.

### Iniciar la Interfaz de Python

Para comenzar a trabajar con Python, necesitamos iniciar un programa que interprete y ejecute nuestros comandos de Python. A continuación, enumeramos varias opciones. Si no tienes una preferencia, procede con la opción superior de la lista que esté disponible en tu máquina. De lo contrario, puedes usar cualquier interfaz que desees.

**Opción A: Jupyter Notebook**

Un cuaderno Jupyter Notebook ofrece una interfaz basada en navegador para trabajar con Python. Si instalaste Anaconda, puedes iniciar un cuaderno de dos maneras:

- **Navegador Anaconda**
  - Inicia Anaconda Navigator. Es posible que te pregunte si deseas enviar información de uso anónima a los desarrolladores de Anaconda: elige tu opción y haz clic en el botón "Aceptar y no mostrar nuevamente".
  - Busca la pestaña “Notebook” y haz clic en el botón “Iniciar”.
  - Anaconda abrirá una nueva ventana o pestaña del navegador con un Panel de Notebook que te mostrará el contenido de tu carpeta de Inicio (o Usuario).
  - Navega hasta el directorio `data` haciendo clic en los nombres de directorio que conducen a él: Escritorio, swc-python, luego `data`.
  - Inicia el cuaderno haciendo clic en el botón “Nuevo” y luego seleccionando “Python 3”.

- **Línea de comandos (Terminal)**
  1. Navega hasta el directorio `data`:
     - **Concha de Unix**: `cd ~/Desktop/swc-python/data`
     - **Windows**: `cd %HOMEPATH%\Desktop\swc-python\data`
  2. Inicia el servidor Jupyter Notebook:
     - **Concha de Unix**: `jupyter notebook`
     - **Windows**: `jupyter notebook`

**Opción B: IPython**

IPython es otro entorno interactivo basado en consola para Python. Es el predecesor del cuaderno Jupyter y, aunque se usa principalmente para aprender y realizar cálculos interactivos, también se puede usar para análisis de datos y programación.

Para comenzar con IPython:

- **Línea de comandos (Terminal)**
  1. Navega hasta el directorio `data`:
     - **Concha de Unix**: `cd ~/Desktop/swc-python/data`
     - **Windows**: `cd %HOMEPATH%\Desktop\swc-python\data`
  2. Inicia IPython:
     - **Concha de Unix**: `ipython`
     - **Windows**: `ipython`

**Opción C: Otros IDEs y Editores de Texto**

También puedes utilizar otros IDEs o editores de texto para escribir y ejecutar tus scripts de Python, como PyCharm, Spyder o Visual Studio Code. Estos entornos generalmente tienen características integradas para ejecutar y depurar scripts de Python.

### Acceso a Datos de Ensayo Clínico

El archivo `inflammation-01.csv` contiene datos de inflamación de 60 pacientes a lo largo de 40 días. La lectura y procesamiento de estos datos se hará en Python usando la biblioteca `pandas`.

**Lectura del archivo CSV**

```python
import pandas as pd
```

# Cargar los datos desde el archivo CSV
data = pd.read_csv('inflammation-01.csv', header=None)

# Mostrar las primeras filas del archivo para verificar su contenido
print(data.head())
