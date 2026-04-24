# Comparación de Modelos de Clasificación en Titanic

Proyecto de análisis y comparación de modelos clásicos de _Machine Learning_ para clasificación binaria, usando el dataset de Titanic.

## Descripción

En este proyecto se comparan distintos algoritmos supervisados para predecir la variable **`survived`** (si una persona sobrevivió o no al accidente del Titanic).

Modelos evaluados:

- Regresión Logística
- Árbol de Decisión
- Random Forest
- SVM (kernel RBF)
- K-Nearest Neighbors (KNN)
- Naive Bayes (GaussianNB)

El análisis incluye:

- Preparación de datos (selección de variables, split train/test, escalado)
- Entrenamiento de modelos
- Métricas de desempeño (`Accuracy`, `AUC`)
- Curvas ROC
- Comparación de tiempo de inferencia

## Estructura del repositorio

- `06_comparacion_modelos_gael_sanchez.ipynb`: notebook principal con todo el flujo de trabajo.
- `Titanic-Dataset.csv`: dataset local del proyecto.
- `requirements.txt`: dependencias necesarias.

## Requisitos

- Python 3.10+ (recomendado)
- Jupyter Notebook

Instalación de dependencias:

```bash
pip install -r requirements.txt
```

## Cómo ejecutar

1. Clona el repositorio.
2. Instala dependencias:

```bash
pip install -r requirements.txt
```

3. Ejecuta Jupyter:

```bash
jupyter notebook
```

4. Abre el archivo:

```text
06_comparacion_modelos_gael_sanchez.ipynb
```

5. Corre las celdas en orden.

## Variables y preprocesamiento (resumen)

- Variable objetivo: `survived`
- División: `train/test` con `test_size=0.2` y `random_state=42`
- Escalado: `StandardScaler` para modelos sensibles a escala (LogReg, SVM, KNN)

## Resultados destacados del notebook

Métricas reportadas en salidas del notebook:

| Modelo                   | Accuracy |    AUC |
| ------------------------ | -------: | -----: |
| Regresión Logística      |   0.7901 | 0.8523 |
| Árbol de Decisión        |   0.7634 |      - |
| Random Forest            |   0.7939 | 0.8579 |
| SVM (RBF)                |   0.4046 | 0.8426 |
| KNN                      |   0.4237 | 0.6984 |
| Naive Bayes (GaussianNB) |   0.7595 | 0.8262 |

Hallazgos finales del notebook:

- **Mejor Accuracy:** `RF`
- **Mejor AUC:** `RF`
- **Modelo más rápido:** `LogReg`

## Conclusión

De acuerdo con la comparación realizada, **Random Forest** presenta el mejor balance entre desempeño y estabilidad para este problema.

## Autor

**Yosef Gael Sanchez Franco**

## Licencia

Este proyecto se comparte con fines académicos.
