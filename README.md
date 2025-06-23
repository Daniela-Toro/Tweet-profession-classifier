# Tweet Profession Classifier 🧠🇪🇸

Este proyecto entrena un modelo de aprendizaje automático para **clasificar tweets en español** según si **mencionan o no una profesión**. Está diseñado para tareas de análisis de contenido en redes sociales, minería de texto o estudios sociolingüísticos.

> 🔧 Desarrollado íntegramente en **Google Colaboratory**, utilizando Python y librerías de NLP modernas como Hugging Face 🤗 Transformers.

---

## 📊 Objetivo

Entrenar un modelo BERT en español para clasificar tweets en dos clases:
- **Clase 0 (SIN_PROFESIÓN)**: No menciona profesiones.
- **Clase 1 (CON_PROFESIÓN)**: Menciona profesiones explícitamente.

---

## 🧪 Métricas del mejor modelo

| Clase                | Precisión | Recall | F1-Score |
|----------------------|-----------|--------|----------|
| **SIN_PROFESIÓN (0)** | 0.98      | 0.94   | 0.96     |
| **CON_PROFESIÓN (1)** | 0.83      | 0.95   | 0.89     |

> Accuracy total: **93.8%**  
> F1 macro promedio: **0.938**

---

## 🧼 Preprocesamiento

- Tokenización con HuggingFace `AutoTokenizer`

---

## 🧾 Fuente de Datos

Utilizamos un subconjunto de datos provenientes de redes sociales, específicamente de la tarea 1 del shared task [**ProfNER**](https://temu.bsc.es/smm4h-spanish), centrado en la detección de menciones a profesiones en tweets publicados durante la pandemia del COVID-19.

El objetivo original de dicha tarea era analizar qué profesiones podrían haber sido especialmente vulnerables en el contexto de la crisis sanitaria.

Descargamos los datos del [repositorio de Hugging Face](https://huggingface.co/datasets/luisgasco/profner_classification_master), en el que se incluyen:

- **Datos de entrenamiento**: con identificadores, texto y etiquetas.
- **Datos de validación**: misma estructura que el conjunto de entrenamiento.
- **Datos de prueba (test)**: incluye identificadores y texto, pero **sin etiquetas**.

---

## 🤖 Modelo

- Modelo base: [`dccuchile/bert-base-spanish-wwm-cased`](https://huggingface.co/dccuchile/bert-base-spanish-wwm-cased)
- Entrenado con `transformers.Trainer`

---

## 🧪 Librerías necesarias

```bash
pip install numpy==1.26.4 fsspec==2023.9.2 transformers datasets evaluate accelerate bitsandbytes transformers-interpret scikit-learn


