# Brief del Proyecto: Análisis horario de la relación entre la radiación solar, velocidad del viento y eventos de precipitación en el Valle de Aburrá

## 1. Pregunta de análisis
¿Cómo varían la radiación solar y la velocidad del viento a escala horaria antes, durante y después de los eventos de precipitación en el Valle de Aburrá?

## 2. Quién decide
Equipo de análisis hidrometeorológico y gestión del riesgo ambiental en el Valle de Aburrá (contexto académico).

## 3. Fuente de datos
Registros meteorológicos horarios públicos de estaciones automáticas del Sistema de Alerta Temprana de Medellín y el Valle de Aburrá (SIATA), en formato CSV.

## 4. Alcance
- Exploración y análisis descriptivo mediante SQL de series horarias de radiación solar, velocidad del viento y precipitación.
- Comparación del comportamiento horario de radiación y viento en horas con precipitación frente a horas secas.

## 5. Qué NO incluye
- Pronósticos meteorológicos ni modelación climática en tiempo real.
- Datos personales de operadores ni estaciones privadas restringidas.
- Variables de calidad del aire o niveles hidrológicos de quebradas y ríos.

## 6. Riesgos de calidad de los datos
- **Datos faltantes (NULL):** Vacíos horarios por fallas de transmisión o mantenimiento en las estaciones del SIATA.
- **Valores atípicos (Outliers):** Lecturas extremas o erróneas por descalibración temporal de los sensores.
- **Asimetría en lluvia:** Gran proporción de horas con precipitación igual a `0.0 mm`, lo que exige separar bien los eventos de lluvia al promediar.
