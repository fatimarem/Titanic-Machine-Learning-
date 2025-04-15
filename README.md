# 🛳️ Predicción de Supervivencia en el Titanic con KNN

Este proyecto tiene como objetivo predecir la probabilidad de supervivencia de los pasajeros del Titanic utilizando el algoritmo de clasificación **K-Nearest Neighbors (KNN)**. El dataset utilizado proviene de la competencia de Kaggle: [Titanic: Machine Learning from Disaster](https://www.kaggle.com/c/titanic/data).

---

## 🎯 Objetivo

Desarrollar un modelo de machine learning que prediga si un pasajero sobrevivió o no al hundimiento del Titanic, a partir de características como edad, sexo, clase, etc.

---

## 📁 Datos utilizados

- `train.csv`: Datos con etiquetas (para entrenamiento)
- `test.csv`: Datos sin etiquetas (para predicción)
- `gender_submission.csv`: Contiene la columna `Survived` para los datos de testing, usada para validación

---

## ⚙️ Herramientas utilizadas

- Python
- Pandas, NumPy
- Seaborn, Matplotlib
- Scikit-learn

---

## 🧪 Proceso de trabajo

### 1. Carga y combinación de datos

Se cargaron los datasets y se añadió la columna `Survived` al dataset de test desde `gender_submission.csv`.

### 2. Limpieza y tratamiento de valores nulos

- Se eliminaron columnas con demasiados valores nulos (`Cabin`)
- Se imputaron valores faltantes en `Age`, `Fare` y `Embarked` usando criterios como mediana o moda

### 3. Análisis exploratorio (EDA)

Se visualizaron relaciones entre variables y la supervivencia:
- Supervivencia por clase (`Pclass`)
- Supervivencia por sexo (`Sex`)
- Distribución de tarifas (`Fare`)

### 4. Feature Engineering

- Se crearon variables dummies para `Pclass`, `Sex` y `Embarked`
- Se eliminó información irrelevante como `Name`, `Ticket` y `PassengerId`
- Se creó la variable `IsMinor` para indicar si un pasajero era menor de edad (≤16 años)

### 5. Entrenamiento del modelo

Se entrenó un modelo **KNN con k=5** sobre el conjunto de entrenamiento, utilizando todas las variables relevantes.

### 6. Evaluación del modelo

Se aplicó el modelo al conjunto de test y se evaluaron los resultados con:

- Matriz de confusión
- Accuracy: **65.3%**
- Sensibilidad: **53.3%**
- Especificidad: **72.2%**

---

## 📈 Resultados

El modelo logra una precisión razonable considerando su simplicidad. Las variables más influyentes fueron el **sexo**, la **edad** y la **clase del pasajero**.

---


