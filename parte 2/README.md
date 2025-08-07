# 📊 Predicción de Evasión de Clientes en Servicios de Telecomunicaciones

Este proyecto busca predecir la cancelación de clientes (`churn`) en una empresa de telecomunicaciones ficticia llamada **Telecom X**, utilizando técnicas de aprendizaje automático. A través del análisis de datos, modelado predictivo y evaluación de métricas, se identifican los principales factores que influyen en la decisión de abandonar el servicio y se proponen estrategias de retención.

---

## ⚙️ Tecnologías utilizadas

- Python 3.13+
- Jupyter Notebook
- Pandas
- NumPy
- Matplotlib / Seaborn
- Scikit-learn
- XGBoost
- imbalanced-learn (SMOTE)

---

## 🔍 Objetivo del proyecto

- Identificar los factores que más influyen en la **cancelación de clientes**.
- Construir modelos predictivos para anticipar la **probabilidad de churn**.
- Proponer **estrategias de retención** basadas en resultados cuantitativos.

---

## 🧪 Flujo de trabajo

1. **Carga y limpieza de datos**

   - Validación de tipos, valores nulos y duplicados.
   - Eliminación de variables redundantes (`Cargo Diario`, `Cargo Total`).

2. **Análisis exploratorio (EDA)**

   - Distribución de la variable objetivo.
   - Boxplots de permanencia y cargos.
   - Matriz de correlación.

3. **Preprocesamiento**

   - Codificación de variables categóricas.
   - Feature Engineering: cálculo de servicios contratados.
   - División Train/Test.

4. **Modelos base**

   - Regresión Logística.
   - Árbol de Decisión.
   - Métricas: accuracy, precision, recall, F1, AUC.

5. **Balanceo de clases**

   - SMOTE aplicado a la clase minoritaria.
   - Evaluación con Random Forest y XGBoost.

6. **Optimización de hiperparámetros**

   - `GridSearchCV` con validación cruzada.
   - Mejora significativa de Recall en clase positiva.

7. **Análisis de importancia de variables**

   - Variables más influyentes: tipo de contrato, permanencia, cargos, servicios digitales.

8. **Recomendaciones y estrategias de retención**
   - Ver en el informe final.

---

## 🧠 Resultados clave

- **Modelo final**: Random Forest optimizado
- **AUC**: 0.8258
- **Recall clase 1 (evasión)**: 0.6417
- **Variables clave**:
  - Tipo de contrato
  - Permanencia
  - Cargo mensual
  - Número de servicios contratados

---

## 📌 Conclusiones

El modelo permite identificar clientes con alto riesgo de cancelación, facilitando la toma de decisiones estratégicas en campañas de retención. Se recomienda enfocar esfuerzos en mejorar condiciones para contratos mensuales y ofrecer beneficios exclusivos a clientes con baja permanencia.

---

## 📄 Informe completo

Puedes consultar el informe detallado para el cliente [aquí](./informe_final.md).

---

## ✅ Requisitos

Instalar las dependencias:

```bash
pip install -r requirements.txt
```

**Autor:** Elias Celis - [LinkedIn](httpshttps://www.linkedin.com/in/ecelis)
