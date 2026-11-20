# 📉 TPI Grupo 3 — Análisis de Cancelación de Clientes (Churn) — Telco Customer Churn

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Lea-2005/tpi-analisis-de-datos-grupo-3/blob/main/notebooks/TPI_Analisis_de_Datos.ipynb)
![Python](https://img.shields.io/badge/Python-3.10%2B-3776AB?logo=python&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-150458?logo=pandas&logoColor=white)
![Estado](https://img.shields.io/badge/estado-en%20desarrollo-yellow)

Trabajo Práctico Integrador de **Introducción al Análisis de Datos** (2º cuatrimestre 2026).

---

## 🎯 Problema de negocio

Una empresa de telecomunicaciones pierde cada mes alrededor de **1 de cada 4 clientes**, que dan de baja el servicio (*churn*). Retener a un cliente existente cuesta mucho menos que conseguir uno nuevo, así que la empresa necesita entender **qué características tienen los clientes que se van**: datos sociodemográficos, tipo de contrato, servicios contratados y facturación.

Este proyecto analiza el historial de **7.043 clientes** para:
- Identificar los **segmentos con mayor riesgo de baja**.
- Contrastar hipótesis sobre el efecto del tipo de contrato, la antigüedad, el precio y el medio de pago.
- Proponer **acciones de retención** basadas en datos.

**Variable de interés:** `Churn` (*Yes* / *No*).

## 👥 Integrantes — División 143

| Integrante | GitHub |
|---|---|
| Mamani, Leandro | [@Lea-2005](https://github.com/Lea-2005) |
| Leyes, Agustín | [@Agustin-Leyes](https://github.com/Agustin-Leyes) |
| Guantay, Marcos | [@MarcosGuantay23](https://github.com/MarcosGuantay23) |
| Verdecanna, Luciano | [@LucianoVerdecanna](https://github.com/LucianoVerdecanna) |

**Docente:** Zotti, Enzo Martín

## 🚀 Cómo explorar el proyecto

### Opción 1 — Google Colab (recomendada)
1. Hacé clic en el badge **Open in Colab** de arriba.
2. En Colab: **Entorno de ejecución → Ejecutar todas**.
3. Listo. No hay que instalar nada ni subir archivos: el dataset se descarga automáticamente.

### Opción 2 — Ejecución local
```bash
git clone https://github.com/Lea-2005/tpi-analisis-de-datos-grupo-3.git
cd tpi-analisis-de-datos-grupo-3
python -m venv .venv
source .venv/bin/activate        # En Windows: .venv\Scripts\activate
pip install -r requirements.txt
jupyter notebook notebooks/TPI_Analisis_de_Datos.ipynb
```

### Orden de lectura sugerido
1. Este **README**, para entender el contexto.
2. El **notebook**: código, análisis e interpretaciones paso a paso.
3. El **informe ejecutivo** (`docs/INFORME_EJECUTIVO.pdf`): metodología y conclusiones para la toma de decisiones.

## 📁 Estructura del repositorio

```
.
├── README.md                        # Portada del proyecto (este archivo)
├── requirements.txt                 # Librerías y versiones mínimas
├── .gitignore                       # Archivos excluidos del control de versiones
├── notebooks/
│   └── TPI_Analisis_de_Datos.ipynb  # Notebook principal (ejecutable en Colab)
├── data/
│   ├── README.md                    # Origen y diccionario de datos
│   ├── raw/                         # Dataset original (opcional, el notebook lo descarga)
│   └── processed/                   # Dataset limpio generado por el notebook
├── docs/
│   └── INFORME_EJECUTIVO.pdf        # Informe técnico-ejecutivo con carátula
└── reports/
    └── figures/                     # Gráficos exportados para el informe y la exposición
```

## 🧰 Stack tecnológico

| Herramienta | Uso en el proyecto |
|---|---|
| **Python 3** | Lenguaje principal |
| **Pandas** | Ingesta, limpieza, transformación, filtrado y agregación (`groupby`) |
| **NumPy** | Operaciones numéricas y vectorizadas |
| **Matplotlib** | Base de los gráficos |
| **Seaborn** | Histogramas/KDE, boxplots, heatmap de correlación y gráficos de barras |
| **Google Colab** | Entorno de ejecución reproducible en la nube |
| **Git + GitHub** | Control de versiones y publicación |

## 📊 Dataset

**Telco Customer Churn**: [Kaggle](https://www.kaggle.com/datasets/blastchar/telco-customer-churn) / IBM Sample Data Sets.
7.043 registros × 21 variables: datos sociodemográficos, servicios contratados, contrato, facturación y estado de cancelación.
Ver detalle y diccionario de variables en [`data/README.md`](data/README.md).

## 🗺️ Contenido del análisis

| Sección | Contenido | Estado |
|---|---|---|
| **A. Fundamentos, ingesta y limpieza** | Problema, hipótesis, clasificación de variables, tratamiento de `TotalCharges`, dtypes, outliers (IQR), filtrado, `groupby`, columnas calculadas | ✅ |
| **B. Análisis exploratorio y visualización** | Medidas de tendencia central y dispersión, correlación de Pearson, tablas de contingencia, histogramas/KDE, heatmap, barras de churn | ⏳ |
| **C. Reproducibilidad** | Colab, semilla fija, controles automáticos, Git, README | ✅ |

## ♻️ Reproducibilidad

- El notebook se ejecuta **de principio a fin sin errores** con *Reiniciar y ejecutar todas*.
- Los datos crudos no se modifican: toda la limpieza se hace por código y queda documentada.
- Solo se usan **rutas relativas** y una **URL pública** para los datos.
- Hay una **semilla fija** (`SEMILLA = 42`) y **controles automáticos** (`assert`) que validan el dataset limpio.
- Las versiones de las librerías se imprimen al final del notebook.
