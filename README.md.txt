# Tabular GAN for Synthetic Medical Records 🏥

Este proyecto utiliza **Generative Adversarial Networks (GANs)** para generar datos sintéticos a partir de registros médicos de seguimiento. El objetivo es demostrar cómo la IA puede crear datos tabulares realistas que preserven la privacidad de los pacientes.

## 📋 Descripción del Proyecto
El modelo aprende la distribución estadística de un dataset de seguimiento de salud que incluye variables como:
- Signos vitales (Presión arterial, IMC, Frecuencia cardíaca).
- Biomarcadores (Glucosa, HbA1c, Creatinina, Colesterol).
- Factores de estilo de vida y adherencia a medicamentos.

## 🛠️ Arquitectura
El sistema consta de dos redes neuronales profundas construidas con **PyTorch**:
1. **Generator**: Una red que toma un vector latente (ruido) y lo transforma en un registro médico sintético.
2. **Discriminator**: Una red que clasifica si un registro es real (del dataset original) o sintético (creado por el generador).

## 🚀 Cómo funciona
1. **Preprocesamiento**: Escalado de datos numéricos con `MinMaxScaler` y codificación de categorías con `OneHotEncoder`.
2. **Entrenamiento**: Un bucle de entrenamiento antagónico donde ambas redes mejoran simultáneamente usando una función de pérdida de Entropía Cruzada Binaria (BCELoss).
3. **Inferencia**: El generador produce nuevos datos que luego son transformados inversamente a su escala y formato original.

## 📦 Requisitos
- Python 3.x
- PyTorch
- Pandas
- Scikit-learn
- Numpy

## 📈 Resultados
El script genera un DataFrame final con registros sintéticos listos para ser analizados o utilizados en el entrenamiento de otros modelos de Machine Learning sin riesgo de fuga de datos sensibles.

---
Proyectado desarrollado como parte de mi portafolio en Inteligencia Artificial aplicada a la Salud.