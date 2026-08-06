# Rendimiento académico, vida social y consumo de alcohol

Análisis reproducible en R Markdown de la relación entre salir con amigos (`goout`), consumir alcohol durante los fines de semana (`Walc`) y el rendimiento académico (`G3`), considerando el sexo del estudiante.

## Pregunta de investigación

> ¿Qué relación existe entre salir con amigos, consumir alcohol los fines de semana y el rendimiento académico, considerando el sexo del estudiante?

## Datos

El análisis principal utiliza `student/student-por.csv`, con 649 estudiantes y 33 variables. La carpeta `student/` también contiene la versión de matemáticas, el diccionario y el script de combinación suministrados con el conjunto de datos.

## Resultados principales

- La frecuencia de salir con amigos y el consumo de alcohol de fin de semana están positivamente asociados.
- Las asociaciones bivariadas con la nota final son negativas, pero débiles: rho de Spearman de -0,105 para `goout` y -0,171 para `Walc`.
- En el modelo conjunto, la asociación ajustada entre `Walc` y `G3` es prácticamente nula en mujeres y negativa en hombres, con una interacción estadísticamente significativa.
- El modelo explica 5,6 % de la variabilidad de la nota; los resultados describen asociaciones y no prueban causalidad.

## Archivos principales

- `analisis_rendimiento_por.Rmd`: código y narrativa reproducible.
- `analisis_rendimiento_por.md`: informe en Markdown.
- `analisis_rendimiento_por.html`: informe autocontenido para visualizar en un navegador.
- `figuras_por/`: gráficas generadas, incluido el biplot.
- `Guia de actividades U2 (1).pdf`: guía académica utilizada.

## Reproducción

Se requiere R, RStudio y los paquetes `rmarkdown`, `knitr` y `ggplot2`. Desde la raíz del proyecto:

```r
rmarkdown::render("analisis_rendimiento_por.Rmd")
```

El informe conserva las notas finales iguales a cero porque son válidas según el diccionario e incluye un análisis de sensibilidad sin esos registros.

