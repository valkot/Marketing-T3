# ==========================================
# ARCHIVO 1: README.md
# ==========================================

# M5 Forecasting: Departamento FOODS_3 (California)

Este repositorio contiene una solución avanzada para el pronóstico de series temporales basada en el dataset de la competencia M5 de Walmart. El proyecto implementa un enfoque de **Modelos Globales** utilizando algoritmos de Gradient Boosting para predecir la demanda diaria.

## 📈 Descripción del Proyecto
El sistema se centra en el departamento `FOODS_3` para las tiendas de California (`CA_1`, `CA_2`, `CA_3`, `CA_4`). A diferencia de los métodos estadísticos tradicionales (ARIMA, ETS), este enfoque utiliza **MLForecast** para procesar miles de series temporales simultáneamente, capturando patrones cruzados entre productos.

### Puntos Clave del Desarrollo:
- **Tidy Data:** Transformación de formatos horizontales (días como columnas) a formatos verticales eficientes para modelos de regresión.
- **Feature Engineering:** Generación dinámica de rezagos (lags) y estadísticas móviles (rolling windows).
- **Ensemble Learning:** Combinación ponderada de **LightGBM** y **XGBoost**.
- **Métricas:** Evaluación mediante el Error Porcentual Absoluto Medio (MAPE).



## 🛠️ Requisitos e Instalación
El proyecto requiere Python 3.12+ y las dependencias listadas en `requirements.txt`.

Para asegurar la correcta ejecución del notebook de pronóstico de demanda, es necesario instalar las siguientes librerías. 

```text
# --- Manipulación y Procesamiento de Datos ---
pandas==2.2.2
numpy==1.26.4
scipy

# --- Visualización de Datos ---
matplotlib==3.9.2
seaborn==0.13.2

# --- Modelado de Series Temporales (Core) ---
mlforecast
utilsforecast
window_ops        # Necesaria para cálculos de ventanas móviles en mlforecast

# --- Algoritmos de Machine Learning ---
lightgbm
xgboost
scikit-learn      # Para métricas de evaluación como MAPE
statsmodels

# --- Utilidades y Descarga de Datos ---
kagglehub         # Utilizada para obtener el dataset M5
geopandas         # Para análisis espacial si se requiere
shapely
