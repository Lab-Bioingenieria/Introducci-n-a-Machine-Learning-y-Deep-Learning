# Introducción a Machine Learning y Deep Learning en Biomedicina

Este repositorio contiene una serie de recursos, guías y notebooks interactivos diseñados para aprender los fundamentos de la Programación Orientada a Objetos (POO), Machine Learning (ML) y Deep Learning (DL), aplicados de forma práctica al campo de la **Biomedicina y la Salud**.

---

## 📂 Contenido de los Archivos

A continuación se detalla el propósito de cada uno de los archivos incluidos:

* **`0.data.md`**: Un listado curado de datasets de Kaggle orientados a usos clínicos y biomédicos. Explica qué tipos de datos se utilizan tanto para Machine Learning clásico (datos tabulares sobre indicadores de salud) como para Deep Learning (imágenes médicas, radiografías y diagnósticos complejos emparejados). Es el punto de partida para conseguir datos de práctica reales.
* **`1.POO.ipynb`**: Notebook introductorio sobre Programación Orientada a Objetos (POO). Explica en detalle los cuatro pilares fundamentales (Encapsulamiento, Herencia, Polimorfismo y Abstracción) utilizando ejemplos y analogías netamente clínicas (por ejemplo: objetos tipo `Paciente`, herencia de `Celulas` o polimorfismo en `Farmacos`).
* **`2.pipeline.ipynb`**: Notebook sobre la construcción de flujos de trabajo (*pipelines*) en ciencia de datos de salud. Enseña a estructurar una arquitectura de ingesta, transformación y modelado de datos médicos de forma escalable y ordenada.
* **`3.preprocesing.ipynb`**: Guía detallada sobre el paso crítico de preprocesamiento de datos. Cubre técnicas esenciales para datos biomédicos, como el manejo de valores nulos (pacientes con datos faltantes), normalización de exámenes de laboratorio y codificación de variables categóricas (como síntomas puntuales o diagnósticos categóricos).
* **`4.ML.ipynb`**: Implementación de algoritmos de Machine Learning (ML) clásico aplicado a la salud usando `scikit-learn` o librerías similares. Contiene prácticas ideales para predecir costos médicos, riesgos poblacionales de enfermedades y análisis factorial de variables clínicas.
* **`5.DL.ipynb`**: Introducción avanzada al Deep Learning (DL). Este notebook se enfoca en el uso de Redes Neuronales Profundas (MLP, Convolucionales/CNN) para encontrar patrones sumamente ocultos, procesar historiales masivos y realizar visión computacional para imágenes de radiología.

---

## 🚀 Instrucciones para usar Google Colab en Visual Studio Code

Visual Studio Code (VS Code) tiene la capacidad de funcionar comodamente como un cliente (frontend) que ejecuta su código de Python en un entorno súper-potente alojado en Google Colab, permitiéndote aprovechar GPUs gratuitas sin salir de tu editor favorito.

Existen dos enfoques principales para lograr esto:

### Método 1: Conexión mediante Túneles SSH (El método recomendado)

Para tener VS Code conectado plenamente a la máquina virtual (Compute) de Google Colab:

1. **Abre un Notebook vacío en [Google Colab](https://colab.research.google.com/)** en tu navegador.
2. **Instala y configura un túnel de acceso** ejecutando el siguiente código en el notebook de Colab (usaremos `cloudflared` como ejemplo):
   ```python
   # Ejecuta esto en una celda de Google Colab
   !pip install colabcode
   from colabcode import ColabCode
   ColabCode(port=10000, password="tu_contraseña_segura", authtoken="tu_token_ngrok_opcional")
   ```

   *(Nota: Existen otros métodos usando la extensión `colab-ssh` y configurando tus llaves)*.
3. Al ejecutar el bloque anterior, Colab generará una **URL o un comando SSH**.
4. **En tu entorno de VS Code en la PC**, necesitas tener la extensión **Remote - SSH** instalada.
5. Abre la paleta de comandos de VS Code (`Ctrl+Shift+P` en Windows/Linux o `Cmd+Shift+P` en Mac), busca **"Remote-SSH: Connect to Host..."** e introduce el comando de usuario/IP generados por tu Colab.
6. ¡Listo! Puedes abrir tu carpeta de proyectos y utilizar las GPUs gratuitas desde la terminal de VS Code y sus extensiones interactivas de Python.

### Método 2: Usar Google Colab usando tu PC Local (Entorno de Ejecución Local)

Si prefieres usar la interfaz web de Google Colab, pero que el código corra en tu PC (usando los archivos exactos de tu carpeta actual), haz lo siguiente:

1. Asegúrate de tener instalada la extensión oficial de **Jupyter** en VS Code u operar Jupyter en terminal.
2. Abre tu terminal (Command Prompt/Bash) y permite permisos a Colab corriendo:
   ```bash
   pip install jupyter_http_over_ws
   jupyter serverextension enable --py jupyter_http_over_ws
   jupyter notebook --NotebookApp.allow_origin='https://colab.research.google.com' --port=8888 --NotebookApp.port_retries=0
   ```
3. Esto abrirá un servidor Jupyter local y te mostrará un link en la consola con un *token* (revisar la consola).
4. Ve al navegador a Google Colab. En la parte superior derecha donde dice **"Conectar"**, dale click a la flecha hacia abajo y selecciona **"Conectarse a un entorno de ejecución local"**.
5. Allí pegas el link que arrojó tu terminal (el que tiene `?token=...`) y se vinculará para leer tus archivos y ejecutar tu proceso localmente manteniendo la UI de Colab.

Welcome to fish, the friendly interactive shell
Type help for instructions on how to use fish
hombrenaranja@hombrenaranja-Lenovo-V14-G2-ALC ~> git clone git@github.com:Lab-Bioingenieria/practicas-comunitarias-PAOII.git
Cloning into 'practicas-comunitarias-PAOII'...
ssh: connect to host github.com port 22: Connection refused
fatal: Could not read from remote repository.

Please make sure you have the correct access rights
and the repository exists.
hombrenaranja@hombrenaranja-Lenovo-V14-G2-ALC ~ [128]> ls
Arduino/  Desktop/  Documents/  Downloads/  Music/  Pictures/  Public/  Templates/  Videos/  home/  snap/  subir.sql
hombrenaranja@hombrenaranja-Lenovo-V14-G2-ALC ~> git clone git@github.com:Lab-Bioingenieria/practicas-comunitarias-PAOII.git
Cloning into 'practicas-comunitarias-PAOII'...
ssh: connect to host github.com port 22: Connection refused
fatal: Could not read from remote repository.

Please make sure you have the correct access rights
and the repository exists.
hombrenaranja@hombrenaranja-Lenovo-V14-G2-ALC ~ [128]> git clone git@github.com:KevinFernandez21/v0-mobile-therapy-app.git
Cloning into 'v0-mobile-therapy-app'...
ssh: connect to host github.com port 22: Connection refused
fatal: Could not read from remote repository.

Please make sure you have the correct access rights
and the repository exists.
hombrenaranja@hombrenaranja-Lenovo-V14-G2-ALC ~ [128]> git clone git@github.com:KevinFernandez21/v0-mobile-therapy-app.git
Cloning into 'v0-mobile-therapy-app'...
ssh: connect to host github.com port 22: Connection refused
fatal: Could not read from remote repository.

Please make sure you have the correct access rights
and the repository exists.
hombrenaranja@hombrenaranja-Lenovo-V14-G2-ALC ~ [128]> cd Desktop/
hombrenaranja@hombrenaranja-Lenovo-V14-G2-ALC ~/Desktop> git clone git@github.com:KevinFernandez21/v0-mobile-therapy-app.git

Cloning into 'v0-mobile-therapy-app'...
ssh: connect to host github.com port 22: Connection refused
fatal: Could not read from remote repository.

Please make sure you have the correct access rights
and the repository exists.
hombrenaranja@hombrenaranja-Lenovo-V14-G2-ALC ~/Desktop [128]>

> **Importante:** Recuerda que las sesiones de Colab en la nube son temporales. Si cargas tus archivos directamente al Colab remoto (Método 1 sin montar tu Drive o Repositorio de GitHub), **procura descargar o hacer Push a GitHub tus cambios antes de cerrar la sesión** o perderás las ediciones de tus Notebooks.
