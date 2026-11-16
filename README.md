# Estimación de Precios de Referencia para Anfitriones Pequeños de Airbnb en Bogotá 
**Maestría en Inteligencia Analítica de Datos (MIAD) — Universidad de los Andes**
**Proyecto:** Gerencia de Proyectos de Analítica (Entrega 4)
**Grupo 5:** 
* Edgar Iván Morales Rojas
* Juan Camilo Piñeros Guzmán
* Juan Esteban Carrero Herrera
* Manuel Guillermo González Panesso

--- 

## 📌 Descripción del Proyecto
El mercado de alquileres de corta estancia en Bogotá presenta una asimetría de información que afecta a los anfitriones independientes o pequeños (propietarios de 1 o 2 anuncios, quienes representan el **41.4% de la oferta total**). Muchos de estos anfitriones fijan sus tarifas mediante intuición o comparaciones informales, lo que resulta en pérdidas de ocupación por sobreprecio o pérdidas de ingresos por subprecio. 

Este proyecto desarrolla un pipeline analítico y de aprendizaje automático que audita la calidad de los datos raspados de **Inside Airbnb Bogotá**, aplica técnicas cuantitativas de limpieza e imputación, realiza análisis exploratorio (EDA) y entrena un modelo de regresión supervisada (**LightGBM**) para ofrecer tarifas de referencia competitivas con soporte explicativo mediante valores SHAP. 

---

## 📁 Estructura del Repositorio 

```text
proyecto-airbnb-bogota/
│
├── README.md # Guía de instalación, estructura y ejecución
├── requirements.txt # Dependencias de Python necesarias
│
├── data/ # Conjuntos de datos del proyecto (archivos locales)
│  ├── listings0626.csv.gz # Captura de entrenamiento (Junio 2026 - 19,187 registros)
│  ├── listings0926.csv.gz # Captura de evaluación (Septiembre 2026 - 19,505 registros)
│  └── neighbourhoods.geojson # Polígonos de las 20 localidades del Distrito Capital
│
└── Scripts
   ├── CaracteristicasCalidadDatos.ipynb
   └── TecnicasLimpieza.ipynb
