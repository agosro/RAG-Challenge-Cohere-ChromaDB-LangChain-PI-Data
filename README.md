# 📌 README – Challenge 3: *Vector Search con ChromaDB + Cohere + LangChain Text Splitters*

## 🧠 Descripción del Proyecto

Este proyecto corresponde al **Challenge 3 del programa Get Talent Ai Engineer**, en el que implementé un pipeline completo de **procesamiento de texto, vectorización y búsqueda semántica** utilizando:

* **Cohere AI** para generar embeddings.
* **ChromaDB** como base de datos vectorial.
* **Scikit-learn** para métricas (cosine similarity).
* **LangChain Text Splitters** para realizar *chunking* eficiente del texto.
* **Python + Jupyter Notebook** dentro de un entorno virtual (*venv*).

El objetivo fue crear un flujo que permita **cargar un texto**, **dividirlo en chunks**, **convertirlos en embeddings**, almacenarlos en Chroma, y finalmente realizar **búsquedas semánticas** para encontrar los fragmentos más relevantes.

---

## ⚙️ Funcionalidades Implementadas

### ✔️ 1. Carga del texto desde un string

El archivo no se lee desde el sistema local; el contenido se pasa directamente como variable de Python.

### ✔️ 2. División del texto (chunking)

Usé **RecursiveCharacterTextSplitter**, que mantiene coherencia semántica y evita cortes bruscos.

### ✔️ 3. Generación de embeddings (Cohere)

Cada chunk se transforma en un embedding vectorial.

### ✔️ 4. Inserción en ChromaDB

Los embeddings y sus metadatos quedan guardados en la colección.

### ✔️ 5. Búsqueda semántica

El usuario ingresa una pregunta y el sistema devuelve:

* el chunk más similar,
* el score de similitud (cosine similarity),
* el texto del fragmento relevante.

### ✔️ 6. Uso de entorno virtual

Todo corre dentro de un `venv` configurado con Python 3.11.

---

## 📁 Estructura del Proyecto

```
Challenge-3/
│── data/
│     └── Historias.pdf  
├── venv/                 # Entorno virtual
├── requirements.txt      # Dependencias reales del proyecto
├── challenge3.ipynb      # Notebook con el pipeline completo
└── README.md             # Este archivo
```

---

## 📦 Dependencias Principales (se instalan vía requirements.txt)

* cohere
* chromadb
* scikit-learn
* langchain-core
* langchain-text-splitters
* python-dotenv
* jupyterlab
* ipywidgets

---

## 🚀 Flujo General del Código

1. **Importación de librerías**
2. **Carga del texto**
3. **Chunking con LangChain**
4. **Creación de embeddings usando Cohere**
5. **Guardado en ChromaDB**
6. **Consulta semántica del usuario**
7. **Cálculo de similitud y retorno del mejor chunk**

---

## 🧪 Resultados Obtenidos

El sistema devuelve de forma consistente el fragmento más cercano a la pregunta basada en el contenido original, verificando que el pipeline funcione correctamente.

---

## ✨ Autor

**Agostina Torres**
Challenge 3 – Pi Data Science & AI Engineering

---