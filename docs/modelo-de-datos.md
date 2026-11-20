# Modelo de Datos del Dataset

Este documento describe la estructura del archivo tabular (dataset en formato CSV) obtenido del SIATA para el análisis horario en el Valle de Aburrá. No corresponde a una base de datos relacional con múltiples tablas, sino a un único archivo consolidado por hora y estación.

## Archivo: `datos_meteorologicos_siata.csv`

| Columna | Tipo de dato | Qué significa | Ejemplo |
| :--- | :--- | :--- | :--- |
| `fecha_hora` | Fecha y hora (`TIMESTAMP`) | Fecha y hora exacta de la medición horaria (AAAA-MM-DD HH:MM:SS) | `2026-10-15 14:00:00` |
| `estacion` | Texto (`VARCHAR`) | Nombre o código identificador de la estación meteorológica del SIATA | `Torre_SIATA` |
| `municipio` | Texto (`VARCHAR`) | Municipio del Valle de Aburrá donde se ubica la estación | `Medellín` |
| `radiacion_solar` | Decimal (`FLOAT`) | Radiación solar global promedio en la hora, medida en $W/m^2$ | `684.5` |
| `velocidad_viento` | Decimal (`FLOAT`) | Velocidad promedio del viento en la hora, medida en $m/s$ | `3.2` |
| `precipitacion` | Decimal (`FLOAT`) | Precipitación acumulada durante esa hora, medida en $mm$ | `1.4` |

## Relación y granularidad
- **Granularidad:** Cada fila representa **1 hora de medición en 1 estación** específica.
- **Relación:** Al tratarse de un único dataset plano (CSV), no se cruza con otras tablas externas; las agrupaciones y comparaciones se realizan directamente por `fecha_hora` (franja horaria) y por `estacion` / `municipio`.