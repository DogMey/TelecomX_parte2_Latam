# Análisis de Churn en Clientes de Telecomunicaciones  

Este proyecto tiene como objetivo analizar los factores que influyen en la **deserción de clientes (churn)** en una empresa de telecomunicaciones. Para ello se emplearon **métodos estadísticos y de machine learning**, comparando diferentes enfoques y evaluando cuáles variables tienen mayor peso en la predicción de la salida de los clientes.  

---

## Contenido del Proyecto

1. **Carga y exploración de datos**  
   - Importación del dataset de clientes de telecomunicaciones.  
   - Análisis exploratorio (EDA) para identificar tendencias, correlaciones y distribución de variables.  
   - Limpieza de datos: manejo de valores faltantes, conversión de variables categóricas y normalización de variables numéricas.  

2. **Modelos implementados**  
   Se entrenaron y evaluaron dos enfoques principales:
   - **Regresión logística** → Para interpretar coeficientes y ver la dirección/impacto de cada variable.  
   - **Árbol de decisión** → Para analizar la importancia de las variables en un modelo no lineal y de fácil interpretación.  

3. **Resultados clave**  
   ### Regresión Logística  
   Las variables con mayor impacto (positivo o negativo) en el churn fueron:  
   - `PhoneService` (-3.98) → Reduce la probabilidad de churn.  
   - `InternetService_No` (+2.98) → Aumenta la probabilidad de churn.  
   - `InternetService_Fiber optic` (-2.82) → Reduce la probabilidad.  
   - `OnlineSecurity`, `TechSupport`, `StreamingMovies`, `StreamingTV` → Todas estas, cuando el cliente las tiene, reducen la probabilidad de abandono.  
   - `PaymentMethod_Electronic check` (+1.12) → Aumenta el riesgo de churn.  

   **Conclusión**: los clientes con servicios de valor agregado (seguridad online, soporte técnico, streaming) suelen permanecer más tiempo, mientras que aquellos que pagan con *Electronic check* o no tienen internet muestran mayor riesgo de abandono.  

   ### Árbol de Decisión  
   Las variables más importantes fueron:  
   - `Charges.Total` (0.1279) → Total gastado por el cliente.  
   - `tenure` (0.1235) → Tiempo con la empresa.  
   - `Charges.Monthly` (0.1152) → Costo mensual.  
   - `Cuentas_Diarias` (0.1135) → Nivel de interacción con el servicio.  
   - `PaymentMethod_Electronic check` (0.0856) → Método de pago asociado a mayor churn.  

   **Conclusión**: el gasto total, el tiempo de permanencia y el costo mensual son los principales factores en la predicción. Los clientes que llevan poco tiempo o tienen cargos altos son más propensos a desertar.  

---

## Tecnologías utilizadas

- **Lenguaje**: Python  
- **Librerías principales**:  
  - `pandas`, `numpy` → manipulación y análisis de datos.  
  - `matplotlib`, `seaborn` → visualización.  
  - `scikit-learn` → entrenamiento de modelos de machine learning.  

---

## Insights generales

1. Los servicios adicionales como **seguridad online, soporte técnico y streaming** funcionan como *retentores naturales* de clientes.  
2. Los clientes que **pagan con Electronic check** representan un segmento de mayor riesgo.  
3. Variables financieras como **cargos totales y mensuales** junto con la **antigüedad (tenure)** son determinantes en la permanencia.  
4. Se recomienda enfocar estrategias de retención en clientes **nuevos**, con **altos cargos mensuales** y que utilizan **Electronic check** como método de pago.  

---

## Próximos pasos

- Probar modelos más complejos como **Random Forest** y **Gradient Boosting** para mejorar la precisión.  
- Implementar un sistema de **alerta temprana** que identifique clientes en riesgo en tiempo real.  
- Desarrollar un **dashboard interactivo** para visualizar los factores de churn y tomar decisiones rápidas.  

---

## Conclusión

Este proyecto permitió identificar de manera clara cuáles variables impactan en la deserción de clientes. La combinación de la **interpretabilidad de la regresión logística** y la **capacidad de segmentación del árbol de decisión** ofrece una visión sólida para que la empresa diseñe estrategias efectivas de retención y mejore la satisfacción de sus clientes.  
