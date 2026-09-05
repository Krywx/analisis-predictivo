Análisis Predictivo de Partidas — Counter-Strike: Global Offensive

Proyecto académico (Fundamentos de Machine Learning, Duoc UC) desarrollado en equipo, aplicando la metodología CRISP-DM sobre un dataset real de partidas de CS:GO.

Trabajo en equipo: Cristóbal Rozas Rogazy & Anderson Tineo.

Problema de negocio

Se plantea un caso donde Valve requiere apoyo analítico para entender qué variables influyen en el desempeño de los jugadores y en el resultado de las rondas, con el fin de mejorar el diseño del juego y la experiencia competitiva.

Dataset
~7.000 partidas, 79.157 registros (filas), 29 columnas por jugador/ronda.
Variables incluidas: asesinatos por ronda, tiempo vivo, distancia recorrida, valor del equipamiento, headshots, resultado de la ronda, entre otras.
Metodología (CRISP-DM)
Business Understanding — Definición de hipótesis de negocio: predicción de asesinatos totales por partida (regresión) y predicción del ganador de la ronda (clasificación).
Data Understanding — Análisis exploratorio con Pandas; estadísticos descriptivos, revisión de valores nulos.
Data Preparation — Limpieza de datos (remoción de nulos y columnas irrelevantes), preparación para feature engineering.
Modeling:
Regresión: LinearRegression y RandomForestRegressor, con StandardScaler y GridSearchCV para tuning.
Clasificación: RandomForestClassifier para predecir el ganador de la ronda, con LabelEncoder para variables categóricas.
Evaluation — Métricas de regresión (MSE, R²) y de clasificación (accuracy, matriz de confusión, ROC-AUC, classification report).
Deployment — Serialización del modelo final con joblib (best_model.pkl) para su reutilización.
Herramientas y librerías

Python · Pandas · NumPy · Scikit-Learn · Matplotlib · Seaborn · Joblib

Resultado

El modelo de clasificación (Random Forest) fue seleccionado como el más adecuado por su balance entre precisión, interpretabilidad de importancia de variables, y desempeño tras la optimización de hiperparámetros vía Grid Search con validación cruzada.

Cómo ejecutar
Clonar el repositorio.
Instalar dependencias: pip install pandas numpy scikit-learn matplotlib seaborn joblib
Abrir notebook.ipynb en Jupyter o Google Colab y ejecutar las celdas en orden.
