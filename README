
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
| **Random Forest**    | ⭐ Mayor rendimiento en todas las métricas. |
| Red Neuronal         | Buen desempeño general, balanceado. |
| Árbol de Decisión    | Ligeramente sobreajustado. |
| KNN                 | Menor recall, pero aceptable con normalización. |
| Baseline            | Sirve como referencia (muy bajo rendimiento). |

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

---

## 6. Conclusión

El modelo de **Random Forest** fue el más robusto para predecir la cancelación de clientes. Las variables relacionadas con el tiempo de permanencia, servicios contratados y forma de pago resultan claves para anticipar la evasión.

Con esta información, TelecomX puede diseñar estrategias proactivas que fortalezcan la retención y mejoren la experiencia del cliente.

---
