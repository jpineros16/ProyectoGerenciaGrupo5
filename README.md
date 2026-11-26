# Estimación de Precios de Referencia para Anfitriones Pequeños de Airbnb en Bogotá

**Maestría en Inteligencia Analítica de Datos (MIAD) — Universidad de los Andes**
**Proyecto:** Gerencia de Proyectos de Analítica (Anteproyecto)

**Grupo 5:**
* Edgar Iván Morales Rojas
* Juan Camilo Piñeros Guzmán
* Juan Esteban Carrero Herrera
* Manuel Guillermo González Panesso

---

## 📌 Descripción del Proyecto

El mercado de alquileres de corta estancia en Bogotá presenta una asimetría de información que afecta a los anfitriones independientes o pequeños (propietarios de 1 o 2 anuncios, quienes representan el **41,4 % de la oferta total**). Muchos de estos anfitriones fijan sus tarifas mediante intuición o comparaciones informales, lo que resulta en pérdidas de ocupación por sobreprecio o pérdidas de ingresos por subprecio.

Este proyecto desarrolla el análisis previo a la construcción de una herramienta de precios de referencia para anfitriones pequeños: audita la calidad de los datos raspados de **Inside Airbnb Bogotá**, aplica técnicas cuantitativas de limpieza e imputación y realiza análisis exploratorio (EDA). El modelado y el prototipo web se desarrollarán en el curso de Proyecto Aplicado. En los cuadernos se usa un modelo de referencia preliminar solo para medir el efecto de las decisiones de limpieza sobre el error.

---

## 📁 Estructura del Repositorio

```text
ProyectoGerenciaGrupo5/
│
├── README.md                # Guía de instalación, estructura y ejecución
├── requirements.txt         # Dependencias de Python necesarias
│
├── data/                    # Conjuntos de datos del proyecto (archivos locales)
│   ├── listings0626.csv.gz      # Captura de entrenamiento (junio 2026 - 19.187 registros)
│   ├── listings0926.csv.gz      # Captura de evaluación (septiembre 2026 - 19.505 registros)
│   └── neighbourhoods.geojson   # Polígonos de las 20 localidades del Distrito Capital
│
├── docs/
│   ├── Carta_Proyecto_Ajustada.xlsx    # Carta proyecto ajustada (editable)
│   ├── Carta_Proyecto_Ajustada.pdf     # Carta proyecto ajustada (para consulta)
│   └── Guia3_RBS_AMEF_Grupo5.pdf       # RBS y AMEF con los 23 factores de riesgo
│
└── Scripts/
    ├── CaracteristicasCalidadDatos.ipynb   # Calidad de los datos, exploración, línea base y métrica de negocio
    └── TecnicasLimpieza.ipynb              # Técnicas de limpieza y su efecto en el error
```

---

## ▶️ Cómo ejecutar

1. Instalar las dependencias: `pip install -r requirements.txt`
2. Abrir los cuadernos de la carpeta `Scripts/` con Jupyter. Leen los datos desde `data/`.

---

## 📄 Fuente de los datos y licencia

Datos de [Inside Airbnb](https://insideairbnb.com/get-the-data/) (Bogotá), con licencia CC BY 4.0. Captura de junio: raspada el 21 y 22 de junio de 2026. Captura de septiembre: raspada el 16 de septiembre de 2026.

Los archivos de `data/` son las capturas públicas tal como las entrega Inside Airbnb. Incluyen campos con datos personales de los anfitriones (nombre, descripción, fotos y enlaces), que solo se usan para medir la calidad de los datos. El cuaderno `CaracteristicasCalidadDatos.ipynb` los excluye antes de cualquier análisis, el modelo no los usa y el prototipo no los mostrará.
