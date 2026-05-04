# 🍷 Análisis y Predicción de Calidad del Vino con Redes Neuronales

## Descripción
Proyecto de Machine Learning que predice la calidad de vinos tintos y blancos a partir de sus características fisicoquímicas, comparando el desempeño de una **Red Neuronal (MLPRegressor)** contra una **Regresión Lineal** como modelo base.

## Resultados Obtenidos

| Modelo | MSE | R² |
|--------|-----|-----|
| Red Neuronal (base: 6,6) | 0.4934 | 0.3315 |
| **Red Neuronal (optimizada: 100,50,25)** | **0.4853** | **0.3423** |
| Regresión Lineal | 0.5497 | 0.2551 |

✅ La red neuronal optimizada superó a la regresión lineal en ambas métricas.

## Dataset
- **Fuente:** VinoMaster
- **Muestras:** 6,497 vinos (tintos y blancos)
- **Variables:** 12 características fisicoquímicas (acidez, pH, alcohol, sulfatos, etc.)
- **Variable objetivo:** Calidad del vino (escala 3–9)

## Tecnologías Utilizadas
- Python 3.x
- Pandas & NumPy
- Scikit-learn (MLPRegressor, LinearRegression, StandardScaler)
- Matplotlib & Seaborn

## Estructura del Proyecto
```
├── datos_VinoMaster.csv          # Dataset original
├── proyecto_vino_master.ipynb    # Notebook con análisis completo
└── README.md
```

## Flujo del Proyecto
1. **Carga y limpieza de datos** — pd.read_csv + limpieza de nombres de columnas
2. **Análisis exploratorio** — distribución de calidad, correlaciones, histogramas
3. **Preprocesamiento** — codificación de variables, train/test split (80/20), StandardScaler
4. **Modelado** — MLPRegressor con exploración de 6 arquitecturas diferentes
5. **Comparación** — Red Neuronal vs Regresión Lineal (MSE y R²)

## Visualizaciones Incluidas
- Distribución de la calidad del vino
- Distribución por tipo (tinto vs blanco)
- Mapa de correlación entre variables
- Comparación de predicciones vs valores reales
- Gráfica comparativa de MSE y R² por modelo

## Conclusiones
- La red neuronal optimizada reduce el MSE en ~12% respecto a la regresión lineal
- El **alcohol** es la variable con mayor correlación positiva con la calidad
- El escalamiento de datos (StandardScaler) fue fundamental para el rendimiento de la red
- La arquitectura **(100, 50, 25)** con 3,000 iteraciones fue la configuración óptima

## Autor
 Alejandro Reyes | Analista de Datos Jr.
