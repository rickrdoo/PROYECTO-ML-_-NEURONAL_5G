
<h2 align="center">Modelo Neuronal - Implementaciones 5G por Región</h2>

<p align="center">
 <img src="[https://cdn-icons-gif.flaticon.com/15588/15588914.gif](https://nhanquyen.co/wp-content/uploads/2024/06/5G-8f2779_cb774306c8904da2a2951e99b3700113mv2.gif)" alt="Visualización" width="300"/>
</p>

## 1. Librerías utilizadas
- **pandas / numpy**: Manipulación de datos.
- **matplotlib / seaborn**: Visualización gráfica.
- **scikit-learn**: Preprocesamiento, evaluación y métricas.
- **TensorFlow Keras**: Construcción y entrenamiento del modelo de red neuronal.

### Asegurate de tener instaladas las librerias:
```bash
  pip install numpy
  pip installa pandas
  pip intall matplotlib
  pip intall sickit-learn
```
---
## 2. Dataset
- Archivo CSV: `Reporte_NOKIA_5G_3500.csv`
- Contiene información de sitios con implementaciones 5G por región y fecha de visita.
---

## 3. Preprocesamiento de datos del archiuvo //Reporte_NOKIA_5G_3500.csv//
- Limpieza de nombres de columnas.
- Conversión de fechas.
- Eliminación de valores nulos en campos críticos (`fecha_visita`, `region`, `proyecto`).
- Creación de nueva característica: `día_del_año` para análisis temporal.

---

## 4. Visualizaciones graficas del modelo 

1. **Distribución de sitios implementados por región**  
   → Gráfico de barras que muestra cuántas implementaciones se hicieron por zona geográfica.

2. **Implementaciones por mes**  
   → Línea temporal del total de instalaciones por mes.

3. **Implementaciones por proyecto a lo largo del tiempo**  
   → Variaciones mensuales por tipo de proyecto.

4. **Predicciones vs valores reales**  
   → Visualización de qué tanto acierta el modelo en la clasificación de regiones.

5. **Matriz de correlación**  
   → Relación estadística entre variables numéricas y categóricas transformadas.

---

## 5. Modelo de Machine Learning

- **Tipo de modelo**: Red neuronal densa (Keras).
- **Entrada**: Día del año (`dia_del_año`).
- **Salida**: Región (clasificación multiclase, codificada con one-hot encoding).
- **Arquitectura**:
  - Capa 1: 16 neuronas, activación ReLU.
  - Capa 2: 8 neuronas, activación ReLU.
  - Capa de salida: neuronas igual al número de regiones, activación Softmax.
- **Entrenamiento**:
  - Épocas: 10
  - Batch size: 4
- **Evaluación**:
  - Precisión (`accuracy`)
  - Reporte de clasificación (`classification_report`)
  - Matriz de confusión
  - Gráfico de predicción vs realidad

---

