# Proyecto-Final-

# Análisis de Tendencias Climáticas Globales (2004–2024)

## Contenido del Repositorio

*   `global_climate_co2_anomalies.csv`: El conjunto de datos original utilizado en el proyecto.
*   `[nombre_del_cuaderno].ipynb`: El cuaderno de Google Colab que contiene todo el código fuente, desde la carga de datos hasta el modelado y las conclusiones.
*   `[nombre_de_las_imágenes_generadas]`: Figuras y gráficos generados durante el análisis exploratorio y la evaluación del modelo (e.g., `1_tendencias_globales.png`, `2_matriz_correlacion.png`, etc.).

## Instalación

Este proyecto se desarrolló en Google Colab, lo que simplifica la configuración del entorno. Si deseas ejecutarlo localmente, asegúrate de tener instaladas las siguientes librerías de Python:

```bash
pip install pandas numpy matplotlib seaborn scikit-learn
```

## Uso

1.  **Clonar el repositorio:**
    ```bash
    git clone https://github.com/tu-usuario/nombre-del-repositorio.git
    cd nombre-del-repositorio
    ```
2.  **Abrir en Google Colab:** Sube el archivo `.ipynb` a tu Google Drive y ábrelo con Google Colab. Alternativamente, puedes abrirlo directamente desde GitHub en Colab.
3.  **Ejecutar las celdas:** Ejecuta las celdas del cuaderno secuencialmente para replicar el análisis completo.

El cuaderno incluye secciones para:
*   Carga y preprocesamiento de datos.
*   Limpieza y transformación (simulación de errores y su corrección).
*   Análisis exploratorio de datos (EDA) con visualizaciones.
*   Análisis estadístico (correlaciones, descriptivos).
*   Aplicación de modelos de regresión lineal y Random Forest.
*   Evaluación de modelos e interpretación de resultados.
*   Conclusiones y recomendaciones.

## Fuente de Datos

El conjunto de datos utilizado es "Global Climate & CO₂ Anomalies (1990–2024)", disponible en Kaggle y publicado por Mohan Krishna Thalla. Los datos provienen de fuentes reconocidas como NOAA, Banco Mundial, Our World in Data y Copernicus.

## Hallazgos Clave

*   **Aceleración del Calentamiento:** Todas las variables climáticas (temperatura global, CO₂, calor oceánico, temperatura ártica) muestran una tendencia creciente, con un salto pronunciado entre 2022 y 2024.
*   **Fuertes Correlaciones Climáticas:** Existe una relación muy fuerte entre la anomalía de temperatura global, la anomalía de temperatura ártica y la temperatura de la superficie del mar.
*   **CO₂ y Temperatura:** La correlación entre las emisiones de CO₂ y la temperatura es más evidente a nivel de tendencias globales anuales que al comparar países-año individuales, debido a la naturaleza acumulativa del efecto invernadero.
*   **Riesgo Climático por Continente:** Aunque el aumento de temperatura es global y sincronizado, el riesgo climático varía significativamente entre continentes, con África y Asia presentando mayores niveles de vulnerabilidad.
*   **Transición Energética:** La relación entre la participación de energías renovables y el riesgo climático es contraintuitivamente débil o positiva, lo que puede explicarse por el historial de emisiones acumuladas en economías desarrolladas.

## Modelos Implementados

1.  **Regresión Lineal Múltiple:** Utilizado para predecir el `climate_risk_score` a partir de variables de emisiones y consumo energético. Obtuvo un `R²` bajo (0.04), indicando que estas variables no son los únicos determinantes directos del riesgo climático anual a nivel de país.
2.  **Random Forest Classifier:** Utilizado para predecir la `warming_category` (Normal, Elevado, Alto, Extremo) a partir de anomalías de temperatura. Demostró una alta exactitud (94%), confirmando que las anomalías térmicas son excelentes predictores de la categoría de calentamiento.

## Contribuyentes

*   Nicolas Galvan Gonzalez
*   Nicol Fernanda Garzon Torres
*   Juan Diego Jauregui Rojas
*   Joshua Alexander Rodriguez Amaya
