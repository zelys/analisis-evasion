# Análisis de Evasión de Clientes de Telecomunicaciones

Este proyecto se enfoca en el análisis de la evasión de clientes en una empresa de telecomunicaciones. A través de un proceso de ETL (Extracción, Transformación y Carga), análisis exploratorio de datos (EDA) y modelado de machine learning, se busca identificar los factores que influyen en la decisión de los clientes de abandonar la compañía y construir un modelo predictivo para anticipar futuras evasiones.

**Autor:** Elias Celis - [LinkedIn](https://www.linkedin.com/in/ecelis)

## Estructura del Proyecto

- **`/data`**: Contiene los datos originales en formato JSON y el dataset limpio en formato CSV.
- **`/img`**: Almacena todas las visualizaciones generadas durante el análisis, como gráficos de distribución, correlación y la importancia de las variables.
- **`/parte 1`**: Incluye el notebook `analisis_telecom_1.ipynb`, que detalla el proceso de ETL.
- **`/parte 2`**: Contiene el notebook `analisis_telecom_2.ipynb`, donde se realiza el EDA y el modelado predictivo, y el archivo `informe_final.md` con las conclusiones del estudio.

## Parte 1: Limpieza y Preparación de Datos (ETL)

En el notebook `analisis_telecom_1.ipynb`, se llevaron a cabo las siguientes tareas:

1.  **Extracción**: Se cargaron los datos desde el archivo `TelecomX_Data.json`.
2.  **Transformación**:
    - Se normalizaron las columnas con formato JSON (`customer`, `phone`, `internet`, `account`).
    - Se corrigieron inconsistencias en los datos, como valores faltantes en `Charges.Total` y el tipo de dato de `SeniorCitizen`.
    - Se creó la columna `DailyCharges` para obtener una perspectiva diaria de los cargos.
    - Se tradujeron los nombres de las columnas al español para facilitar el análisis.
3.  **Carga**: El dataset limpio y procesado se guardó en `datos_telecom.csv`.

## Parte 2: Análisis Exploratorio y Modelado (EDA)

El notebook `analisis_telecom_2.ipynb` se centra en el análisis de los datos y la construcción de modelos predictivos:

1.  **Análisis Exploratorio**: Se estudió la distribución de la variable objetivo (`Evasión`) y se analizaron las correlaciones entre las variables.
2.  **Visualizaciones**: Se generaron diversos gráficos para entender mejor la relación entre las características de los clientes y la evasión, incluyendo:
    - Distribución de la evasión, permanencia y cargos.
    - Proporción de evasión por género, tipo de contrato y método de pago.
    - Importancia de las variables según el modelo Random Forest.
3.  **Modelado**:
    - Se entrenaron modelos base de **Regresión Logística** y **Árbol de Decisión**.
    - Se aplicó la técnica **SMOTE** para manejar el desbalance de clases en la variable objetivo.
    - Se entrenaron modelos avanzados como **Random Forest** y **XGBoost** con los datos balanceados.
4.  **Evaluación**: Los modelos fueron evaluados utilizando métricas como _accuracy_, _precision_, _recall_, _F1-score_, la **matriz de confusión** y la **curva ROC**.

## Modelos Utilizados

- Regresión Logística
- Árbol de Decisión
- Random Forest
- XGBoost

## Cómo Utilizar

Para replicar el análisis, se recomienda ejecutar los notebooks en el siguiente orden:

1.  `parte 1/analisis_telecom_1.ipynb`
2.  `parte 2/analisis_telecom_2.ipynb`

Asegúrate de tener instaladas las librerías de Python necesarias, que se importan al inicio de cada notebook.

```bash
pip install -r requirements.txt
```

---
