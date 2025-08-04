
# 📊 Informe Final: Análisis de Cancelación de Clientes - TelecomX

## 1. Objetivo
El presente análisis tiene como propósito predecir la cancelación (churn) de clientes de TelecomX mediante modelos de machine learning y análisis estadístico, con el fin de identificar patrones que permitan implementar estrategias de retención efectivas.

---

## 2. Metodología
Se utilizaron modelos de clasificación para predecir si un cliente cancelará su servicio. Se realizaron las siguientes etapas:
- Preprocesamiento: limpieza de datos, codificación de variables categóricas y normalización.
- Análisis exploratorio: visualización de correlaciones y patrones por churn.
- Balanceo de clases con SMOTE.
- Entrenamiento de modelos: Regresión Logística, Árbol de Decisión, Random Forest, KNN, Red Neuronal.
- Evaluación con métricas: precisión, recall, F1-score y matriz de confusión.
- Análisis de importancia de variables por modelo.

---

## 3. Resultados de Modelado

| Modelo              | Exactitud | Precisión | Recall | F1-score |
|---------------------|-----------|-----------|--------|----------|
| **Random Forest**    | ⭐ Mayor rendimiento en todas las métricas. (0.794605) | 0.643735 | 0.475499 | 0.546973 |
| Red Neuronal         | Buen desempeño general, balanceado. (0.793185) | 0.621277 | 0.529946 | 0.571988 |
| Árbol de Decisión    | Ligeramente sobreajustado. (0.791292) | 0.651099 | 0.430127 | 0.518033 |
| KNN                 | Menor recall, pero aceptable con normalización. (0.760530)| 0.542533 | 0.520871 | 0.531481 |
| Baseline            | Sirve como referencia (muy bajo rendimiento). (0.739233)| 0.000000 | 0.000000 | 0.000000 |

---

## 4. Principales Factores que Influyen en la Cancelación

Los modelos identificaron consistentemente las siguientes variables como más relevantes:

- **Tipo de contrato**: Los contratos mensuales están más asociados con la cancelación.
- **Tenure (meses como cliente)**: Los clientes recientes cancelan con mayor frecuencia.
- **Cargos mensuales**: Cargos más altos están correlacionados con churn.
- **Soporte técnico y seguridad en línea**: La falta de servicios adicionales está vinculada a mayor churn.
- **Método de pago**: Pagos electrónicos automáticos están menos asociados al churn.

---

## 5. Recomendaciones Estratégicas

1. **Fidelización de nuevos clientes**:
   - Implementar beneficios o descuentos progresivos para los primeros meses.
   - Reforzar programas de bienvenida o atención personalizada.

2. **Mejorar servicios complementarios**:
   - Promocionar activamente servicios como respaldo en línea, protección de dispositivos y soporte técnico.

3. **Optimización del pricing**:
   - Evaluar la relación entre cargos mensuales y percepción de valor por parte del cliente.

4. **Revisión de contratos**:
   - Incentivar la migración de contratos mensuales a anuales con beneficios exclusivos.

5. **Automatización del pago**:
   - Promover el uso de débito automático ofreciendo beneficios (descuentos o prioridad de atención).

## 📷 Visualización de Variables Clave en la Cancelación (Churn)

A continuación se presentan las gráficas que respaldan las conclusiones sobre las variables más relevantes en la predicción de la cancelación de clientes:

### 1. Tenure vs Churn (Predicho)
![Tenure](https://github.com/ollin02/Challenge-TelecomX2-Analisis-de-evasi-n-de-clientes/blob/main/Imagenes/Cargos_vs_Churn_Predicho.png)

### 2. Cargos Mensuales vs Churn (Predicho)
![Cargos](https://github.com/ollin02/Challenge-TelecomX2-Analisis-de-evasi-n-de-clientes/blob/main/Imagenes/Tenure_vs_Churn_Predicho.png)

### 3. Tipo de Contrato vs Churn (Predicho)
![Contrato](https://github.com/ollin02/Challenge-TelecomX2-Analisis-de-evasi-n-de-clientes/blob/main/Imagenes/Contrato_vs_Churn_Predicho.png)

### 4. Soporte Técnico vs Churn (Predicho)
![TechSupport](https://github.com/ollin02/Challenge-TelecomX2-Analisis-de-evasi-n-de-clientes/blob/main/Imagenes/TechSupport_vs_Churn_Predicho.png)

### 5. Método de Pago vs Churn (Predicho)
![MetodoPago](https://github.com/ollin02/Challenge-TelecomX2-Analisis-de-evasi-n-de-clientes/blob/main/Imagenes/MetodoPago_vs_Churn_Predicho.png)


## 🎯 Respuestas Estratégicas Clave

### ¿Quiénes son los clientes con mayor riesgo de evasión (churn)?
Los clientes con mayor probabilidad de cancelar sus servicios (churn) son:

- **Clientes con contratos mensuales**, lo que les permite cambiar de proveedor sin penalización.
- **Clientes recientes** (bajo `Tenure`), quienes aún no han generado lealtad hacia la empresa.
- **Usuarios con cargos mensuales altos**, posiblemente perciben un bajo valor por el costo.
- **Clientes que no utilizan servicios adicionales** como soporte técnico o seguridad en línea.
- **Clientes que no tienen automatizado su método de pago**, lo que puede reflejar menor compromiso o comodidad con el servicio.

---

### ¿Qué variables influyen más en ese comportamiento?
Según la importancia de variables extraída de los modelos más robustos (especialmente Random Forest y Redes Neuronales), las variables más influyentes son:

| Variable           | Descripción                                                               |
|--------------------|---------------------------------------------------------------------------|
| `Contract`         | Tipo de contrato: los contratos mensuales tienen más cancelaciones.       |
| `Tenure`           | Tiempo como cliente: a menor tiempo, mayor churn.                         |
| `Charges.Monthly`  | Cargos mensuales: a mayor monto, mayor riesgo de cancelación.             |
| `TechSupport`      | Soporte técnico: su ausencia se asocia a mayor evasión.                   |
| `PaymentMethod`    | Método de pago: automatización se relaciona con menor churn.              |

Estas variables fueron visualizadas en las gráficas que sustentan esta conclusión (ver sección 6 del informe).

---

### ¿Qué perfil de cliente debemos cuidar con mayor atención?
El perfil de cliente con mayor riesgo y que merece mayor atención incluye:

- Nuevos clientes con menos de 1 año en la empresa (`Tenure` bajo).
- Contratos **mensuales**.
- Gasto mensual elevado.
- Sin servicios como **soporte técnico** o **seguridad en línea**.
- Que pagan mediante **métodos manuales** (no automáticos).

📌 **Estrategias sugeridas**:
- **Migrar a contratos anuales** mediante incentivos.
- **Ofrecer soporte técnico gratuito o con descuento** como valor agregado.
- **Promover pagos automáticos** con beneficios como descuentos o atención preferencial.

---

## 6. Conclusión

El modelo de **Random Forest** fue el más robusto para predecir la cancelación de clientes. Las variables relacionadas con el tiempo de permanencia, servicios contratados y forma de pago resultan claves para anticipar la evasión.

Con esta información, TelecomX puede diseñar estrategias proactivas que fortalezcan la retención y mejoren la experiencia del cliente.

---
