# TelecomX2 - Predicción de Churn de Clientes

## 📊 Descripción
Modelo de Machine Learning para predecir la cancelación (churn) de clientes de una empresa de telecomunicaciones (TelecomX).

## 🎯 Objetivo
Desarrollar un modelo predictivo con score ponderado >0.75 para identificar clientes en riesgo de Fuga (churn).

## 📈 Modelos Evaluados
1. **Random Forest Optimizado** - 0.7110 (GANADOR)
2. Regresión Logística Optimizada - 0.6483
3. Random Forest Calibrado - 0.7096

## 🔍 Factores Clave de Churn
1. **Antigüedad Meses** (16.61%) - Clientes nuevos = mayor riesgo
2. **Tipo Contrato Two year** (16.09%) - Contratos largos = retención
3. **Cargo Mensual** (9.80%) - Precio factor decisivo
4. **Tipo Contrato One year** (9.61%)
5. **Servicio Internet Fiber optic** (6.26%)

## 🚀 Estrategias de Retención
- **Programa "Primeros 6 Meses"** para clientes nuevos
- **Incentivos para contratos largos** (1-2 años)
- **Revisión de estructura de precios**
- **Mejora del soporte técnico**

## 🛠️ Tecnologías
- **Python 3.11**
- **Scikit-learn** - Modelos ML
- **Pandas/Numpy** - Manipulación datos
- **Matplotlib/Seaborn** - Visualizaciones
- **SMOTE** - Balanceo de clases


## 🔧 Configuración del Modelo Final
```python
RandomForestClassifier(
    n_estimators=200,
    max_depth=15,
    min_samples_split=20,
    min_samples_leaf=10,
    max_features='sqrt',
    class_weight={0:0.4, 1:0.6}
)
```

## 📊 Dataset
- **Registros:** 9,687 clientes
- **Variables:** 22 características
- **Balance:** 73.5% no churn, 26.5% churn
- **Preprocesamiento:** SMOTE, StandardScaler, feature selection

## 🎯 Implementación
1. **Scoring semanal** de toda la base de clientes
2. **Segmentación por riesgo:** Alto (>0.7), Medio (0.3-0.7), Bajo (<0.3)
3. **Acciones diferenciadas** según nivel de riesgo
4. **Monitoreo continuo** del performance

## 📈 Impacto de Negocio
- **80.21% de churns detectados** antes de que ocurran
- **ROI estimado:** 3:1 a 5:1
- **Ventana de acción:** 1-3 meses promedio

## 🚀 Próximos Pasos
- [ ] Despliegue en producción
- [ ] Dashboard de monitoreo
- [ ] A/B testing de estrategias
- [ ] Modelos avanzados (XGBoost, Neural Networks)
- [ ] Meta: Score ponderado >0.75

## 👤 Autor
**Proyecto desarrollado por:** Londero Guillermo Humberto  
**Programa:** ONE + Alura LATAM - Especialización en Ciencia de Datos  
**Fecha:** Agosto 2025  

### **📞 Contacto**
- **LinkedIn:** www.linkedin.com/in/guillermo-londero
- **GitHub:** https://github.com/GuilleLondero
- **Email:** guillelondero@gmail.com

## 🏆 Reconocimientos
- **Alura + ONE LATAM** por la estructura del desafío
- **Comunidad Data Science** por recursos y mejores prácticas

---

⭐ **Si este proyecto te fue útil, no olvides darle una estrella en GitHub!**

📊 **#DataScience #ChurnAnalysis #TelecomAnalytics #PythonAnalysis #AluraONE**
