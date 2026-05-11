# Conciencia Social: Un Análisis del Bienestar y la Percepción en la UE

## 📌 Descripción del Proyecto
Este proyecto analiza la relación entre los indicadores macroeconómicos (riqueza y gasto público) y las percepciones sociales de los ciudadanos europeos en los 12 países con mayor PIB per cápita de la Unión Europea. El objetivo es identificar si un desarrollo económico sólido se traduce en una mejor percepción social, mayor compromiso civil y mayor conciencia climática y migratoria.

El análisis combina datos de **Eurostat** (indicadores económicos) y la **European Social Survey - ESS** (datos cualitativos de encuestas ciudadanas).

---

## 📊 Visualización (Power BI)
El dashboard se divide en cuatro áreas clave diseñadas para responder preguntas específicas:

1. **Contexto global: perfil del ciudadano europeo:** Análisis de la demografía de la muestra, niveles educativos y confianza institucional y PIB per cápita de los países.
2. **Economía y bienestar: Inversión pública vs. percepción social:** Cruce del PIB per cápita y el gasto público frente a la visión ciudadana sobre temas como la inmigración.
3. **El factor humano: compromiso social y participación:** Perfil de las personas que realizan voluntariado o donaciones según su situación económica/educativa y capacidad política.
4. **Ficha técnica: origen y estructura de datos:** Detalle de las variables y metodología de unión de los datasets.

---

## 🛠️ Preparación y limpieza de datos
Para garantizar la calidad de las visualizaciones, realizamos una fase previa de limpieza y procesamiento utilizando **Python (Pandas)** en Jupyter Notebooks:

### 1. Indicadores de Eurostat (`eurostat_pib_per_capita_inversiones.ipynb`)
* **Acceso a datos:** Uso de la librería `eurostat` para obtener cifras de PIB, habitantes y gastos gubernamentales del año 2022.
* **Limpieza:** Tratamiento de formatos numéricos y preparación de la estructura de tablas para su correcta lectura en Power BI.

### 2. Encuestas de la ESS (`describe_csv_ess.ipynb`)
* **Exploración:** Análisis inicial de los archivos CSV para entender la distribución y codificación de las respuestas.
* **Filtrado:** Selección de los años de estudio (2020 y 2023) y segmentación de los 15 países con mayor PIB per cápita.
* **Tratamiento de variables:** Mapeo y renombrado de categorías cualitativas (niveles educativos, escalas de percepción del 0 al 10) para hacerlas comprensibles en los gráficos.
* **Gestión de valores:** Limpieza de registros incompletos para asegurar la integridad de los promedios y porcentajes.

### 3. Unión de Datasets
* Los datos se conectaron en Power BI mediante el nombre del país como clave común (Left Join), permitiendo que las métricas económicas de Eurostat den contexto a las respuestas individuales de la encuesta social.

---

## 🚀 Tecnologías Utilizadas
* **Python:** Pandas, Eurostat Library, Jupyter Notebooks.
* **Power BI:** Modelado de datos, visualizaciones y medidas DAX.
* **Fuentes:** [Eurostat](https://ec.europa.eu/eurostat) y [European Social Survey (ESS)](https://www.europeansocialsurvey.org/).

---

## 💡 Insights Destacados
* **Inversión y Percepción:** Existe una tendencia que vincula una mayor inversión en gasto social con una percepción más positiva sobre la contribución de la inmigración al país.
* **Educación y Confianza:** Los datos sugieren que a mayor nivel educativo, existe una percepción más optimista sobre el impacto cultural de la diversidad y una mayor confianza institucional.

---

## 📂 Estructura del Repositorio
```bash
├── clean-csv
├── imagenes-para-dashboards
├── original-csv
├── Dashboard_proyecto_modulo_4
├── README.md
├── describe_csv_ess.ipynb
└── eurostat_pib_per_capita_inversiones.ipynb


---
* Este proyecto fue desarrollado dentro del marco del Bootcamp de Data Analysis de Adalab por Eva Ferrer, Saray Hernández y Natalia Pozo.


