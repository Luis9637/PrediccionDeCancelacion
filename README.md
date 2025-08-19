

# 🔍 Análisis Predictivo de Cancelación de Clientes (Churn)

## 🧠 Propósito del Proyecto  
Este repositorio documenta el desarrollo de un modelo de machine learning orientado a anticipar la cancelación de servicios por parte de clientes en una empresa de telecomunicaciones. El objetivo principal es identificar patrones de comportamiento que permitan detectar a tiempo el riesgo de churn y facilitar la toma de decisiones comerciales.  
Este trabajo se enmarca dentro del desafío del programa **ONE de Alura**, en la ruta de especialización en **Ciencia de Datos**.

---

## ⚙️ Metodología de Trabajo

El proyecto se estructuró en las siguientes etapas:

- **Importación de Datos:** Lectura de la base en formato CSV.
- **Limpieza y Preparación:** Depuración de registros duplicados y nulos. Selección de variables relevantes según análisis exploratorio.
- **Transformación de Variables:** Aplicación de codificación One-Hot para convertir variables categóricas en numéricas.
- **Separación de Conjuntos:** División en datos de entrenamiento y prueba.
- **Entrenamiento de Modelos:**
  - **Random Forest:** Pipeline con SMOTE para balancear clases y ajuste de hiperparámetros mediante GridSearchCV.
  - **Regresión Logística:** Pipeline con normalización, SMOTE y evaluación de desempeño.

---

## 📊 Evaluación de Resultados

Se compararon ambos modelos utilizando métricas como **exactitud**, **precisión**, **recall**, **F1-score**, además de la **matriz de confusión** y la **curva ROC**.

- **Random Forest:**  
  - Buen rendimiento general.  
  - Alta precisión en la clase “no churn”, pero menor capacidad para detectar abandonos.

- **Regresión Logística:**  
  - Destaca por su alto **recall** en la clase “churn”, lo que la hace más efectiva para identificar clientes en riesgo, aunque con mayor tasa de falsos positivos.

---

## 🧭 Recomendaciones

La elección del modelo depende del enfoque estratégico:

- Si el objetivo es **reducir la pérdida de clientes**, se recomienda priorizar el **recall** → usar **Regresión Logística**.
- Si se busca **optimizar recursos en campañas de retención**, se recomienda priorizar la **precisión** → usar **Random Forest**.

---

## 📁 Estructura del Repositorio

```
├── data/               # Datos originales y preprocesados
├── notebooks/          # Análisis exploratorio y modelado
├── src/                # Scripts de entrenamiento y evaluación
├── figures/            # Visualizaciones generadas
└── README.md           # Documentación del proyecto
```

---

## 📄 Licencia  
Distribuido bajo la licencia MIT. © Ny-dia

