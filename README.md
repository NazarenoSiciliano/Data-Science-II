# Data-Science-II
# Análisis del Impacto de la Vacunación y Casos de Sarampión en la Provincia de Buenos Aires 🦠💉

## Abstracto
**Motivación:** El sarampión es una enfermedad altamente contagiosa que requiere al menos un 95% de cobertura de vacunación para mantener la "inmunidad de rebaño". Este proyecto analiza el histórico de cobertura de la vacuna Triple Viral (SRP) en la Provincia de Buenos Aires utilizando datos oficiales del Ministerio de Salud (2009-2018). El objetivo a largo plazo es cruzar estos datos con registros de contagios para entrenar un modelo predictivo capaz de identificar riesgos epidemiológicos.
**Audiencia:** Entidades de salud pública, Ministerios de Salud y equipos de epidemiología que busquen optimizar y focalizar campañas de vacunación.

## Preguntas e Hipótesis
1. ¿Se mantuvo la Provincia de Buenos Aires por encima del umbral de seguridad del 95% establecido por la OMS durante la década analizada?
2. ¿Existen disparidades significativas entre la aplicación de la primera dosis (a los 12 meses) y la segunda dosis (al ingreso escolar)?
3. ¿Cuáles fueron los años de mayor riesgo de brote debido a bajas tasas de inmunización?

## Dataset Utilizado
Los datos provienen de la **Dirección de Control de Enfermedades Inmunoprevenibles (DiCEI)** del Ministerio de Salud de Argentina.
- **Archivo:** `dicei-vacunas-srp-2009-2018.csv`
- **Variables principales:** `jurisdiccion_nombre`, Coberturas anuales 1ra y 2da dosis.

## Metodología y Herramientas (Stack Tecnológico)
- **Lenguaje:** Python 3
- **Manipulación de Datos:** Pandas
- **Visualización:** Matplotlib y Seaborn
- **Entorno:** Jupyter Notebook / Google Colab

## Pasos Realizados
1. **Importación:** Carga del dataset desde un archivo local en formato CSV.
2. **Transformación de Datos:** Uso de la función `melt()` de Pandas para pasar el dataset de formato "ancho" (columnas por año) a formato "largo" (series temporales), facilitando su graficación. Extracción de variables como "Año" y "Tipo de Dosis" mediante limpieza de *strings*.
3. **Análisis Exploratorio de Datos (EDA):** Creación de gráficos de líneas visualizando la evolución de ambas dosis contra el umbral del 95% sugerido por la Organización Mundial de la Salud (OMS).

## Insights Preliminares
- A través del EDA, detectamos que en múltiples años (especialmente cerca de 2014-2016), la cobertura de algunas dosis cayó significativamente por debajo del umbral del 95% requerido para evitar la propagación comunitaria. 
- La segunda dosis (ingreso escolar) suele presentar fluctuaciones distintas a la primera dosis (12 meses), lo que invita a investigar sobre la retención de pacientes en el sistema de salud en los primeros 5 años de vida.

## Próximos Pasos (Machine Learning)
En las próximas entregas se planea enriquecer este dataset sumando datos geodemográficos (densidad poblacional por municipio) y el histórico de contagios confirmados para entrenar modelos predictivos (ej: Random Forest o Regresiones) que cataloguen el nivel de alerta sanitaria de cada zona.
