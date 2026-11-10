# Análisis del ROI Social: Fondo SAVE THE NIGHT (Jägermeister)

![Python](https://shields.io)
![spaCy](https://shields.io)
![Status](https://shields.io)

## 📌 Contexto y Problema de Negocio
Desde 2020, el fondo global **SAVE THE NIGHT** de Mast-Jägermeister SE ha evolucionado de una ayuda de emergencia por pandemia a un fondo de innovación social que supera los **156.000 €** anuales. Con casi 1.000 postulaciones de más de 60 países, el desafío del consejo asesor es asegurar que el capital se distribuya de forma equitativa y genere impacto sostenible más allá del evento inicial.

**Pregunta SMART:** *¿Cómo ha evolucionado la distribución geográfica y temática (Seguridad, Inclusión, Sostenibilidad) de los ganadores del fondo SAVE THE NIGHT desde 2022, y qué características se asocian con los proyectos que logran continuidad operativa a largo plazo?*

## 🛠️ Metodología y Stack Tecnológico
El proyecto sigue el ciclo de vida de datos **CRISP-DM** implementado íntegramente en Python:
1. **Recolección (ETL):** Web scraping de comunicados oficiales y prensa especializada mediante `requests` y `BeautifulSoup`.
2. **Procesamiento de Lenguaje Natural (NLP):** Extracción automatizada de entidades nombradas (organizaciones, países, montos) con `spaCy` (`en_core_web_sm`) y clasificación temática por reglas.
3. **Análisis Exploratorio (EDA):** Cálculo de métricas proxy de ROI Social (tasa de supervivencia e índice de descentralización) con `pandas`, `matplotlib` y `seaborn`.

## 📊 Hallazgos Principales
*(Incluye aquí tus gráficos desde la carpeta `reports/figures/`)*

![Distribución de Ganadores](reports/figures/roi_social_analysis.png)

* **Sostenibilidad del impacto:** Los proyectos enfocados en infraestructura permanente o capacitación (pilar *Accesibilidad* y *Seguridad*) muestran una mayor tasa de continuidad operativa frente a eventos puntuales.
* **Descentralización progresiva:** A medida que la bolsa del fondo creció de 50.000 € a 156.000 €, la asignación de recursos se expandió desde Europa hacia mercados emergentes clave en África (Kenia, Sudáfrica) y Latinoamérica (México, Colombia).

## ⚠️ Limitaciones y Recomendaciones de Negocio
* **Limitación de datos:** Al ser datos públicos, la muestra (`n`) se limita a los ganadores anunciados y no incluye el monto exacto asignado individualmente a cada proyecto ni las métricas de las propuestas rechazadas.
* **Recomendación:** Implementar un marco obligatorio de **KPIs de impacto a 12 meses** (ej. personas capacitadas, espacios adaptados, empleos sostenidos) para estandarizar la medición del retorno social en futuras ediciones.

## 🚀 Cómo reproducir este proyecto
1. Clona el repositorio: `git clone https://github.com`
2. Instala las dependencias: `pip install -r requirements.txt`
3. Descarga el modelo de NLP: `python -m spacy download en_core_web_sm`
4. Ejecuta los notebooks en orden numérico dentro de la carpeta `notebooks/`.
