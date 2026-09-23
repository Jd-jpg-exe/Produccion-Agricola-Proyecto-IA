# Producción Agrícola — Proyecto IA I

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Jd-jpg-exe/Produccion-Agricola-Proyecto-IA/blob/main/notebooks/EDA_EVA_Fase1_DEF.ipynb)

Proyecto semestral del curso **Inteligencia Artificial I** (Grupo C2, periodo 2026-2,
Prof. Santiago Gómez) sobre las **Evaluaciones Agropecuarias Municipales (EVA)** de Colombia,
2007–2025.

## Objetivo

Predecir el **área cosechada (hectáreas)** de un cultivo en un municipio a partir de datos
históricos, y evaluar cómo cambia el error de predicción según el horizonte temporal
(+1, +2, +3, +4 periodos).

| Fase | Tema | Estado |
|---|---|---|
| 1 | Análisis exploratorio de datos (EDA) | Entregado |
| 2 | Aprendizaje supervisado | Pendiente |
| 3 | Aprendizaje no supervisado | Pendiente |

## Estructura del repositorio

```
.
├── notebooks/
│   ├── EDA_EVA_Fase1_DEF.ipynb      # Fase 1: limpieza, unión y EDA (versión vigente)
│   └── versiones_anteriores/        # borradores previos, solo como referencia
├── data/
│   ├── raw/                         # CSV originales de las EVA (no se versionan)
│   └── processed/                   # eva_limpio.csv generado por el notebook (no se versiona)
├── docs/
│   └── instrucciones/               # enunciados del curso
└── slides/                          # material de apoyo para las presentaciones
```

## Datos

El notebook usa dos archivos fuente de las EVA (Ministerio de Agricultura y Desarrollo Rural,
publicados en [datos.gov.co](https://www.datos.gov.co/)):

| Archivo | Años | Filas |
|---|---|---|
| `EVA_2007_2018.csv` | 2006–2018 | 206.068 |
| `EVA_2019_2025.csv` | 2019–2025 | 166.732 |

Tras limpiarlos y unirlos quedan **368.475 filas** (32 departamentos, 248 cultivos), y después
de quitar los registros imposibles, **354.505 filas** en `eva_limpio.csv`.

Los CSV **no se suben al repositorio** por tamaño (ver `.gitignore`). Se guardan en Google
Drive, en `MiUnidad/EVA/`.

## Cómo ejecutar el notebook

1. Copia `EVA_2007_2018.csv` y `EVA_2019_2025.csv` a la carpeta `MiUnidad/EVA/` de tu Google
   Drive.
2. Abre el notebook con el botón **Open in Colab** de arriba.
3. Ejecuta todas las celdas (`Entorno de ejecución > Ejecutar todas`) y autoriza el acceso a
   Drive cuando lo pida. Al final se genera `MiUnidad/EVA/eva_limpio.csv` para la Fase 2.

## Flujo de trabajo

El notebook se edita en **Google Colab**, que es la fuente de la verdad. Para guardar una nueva
versión en este repositorio:

`Archivo > Guardar una copia en GitHub` → repositorio `Jd-jpg-exe/Produccion-Agricola-Proyecto-IA`,
rama `main`, ruta `notebooks/EDA_EVA_Fase1_DEF.ipynb`, con un mensaje que describa el cambio.

Usar siempre la misma ruta: así el historial de Git guarda las versiones y no hace falta crear
copias como `_v2`, `(1)`, etc.

## Integrantes

- Iván
- Yerson
- Cristian Gutiérrez
- David Barrera
