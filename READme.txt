🔬 Predicción de Materiales Fotovoltaicos con Machine Learning  
### Ensemble Learning y Análisis de Perovskitas basadas en datos reales del Materials Project

Este repositorio contiene un pipeline completo para **predecir propiedades fotovoltaicas clave** (particularmente Band Gap) en materiales tipo **perovskita**, utilizando:

- Datos reales del **Materials Project (MP)**  
- Modelos avanzados de Machine Learning (Random Forest y XGBoost)  
- Feature engineering físico-químico  
- Análisis comparativo entre modelos  
- Generación automática de rankings de materiales candidatos  

El objetivo principal es **acelerar la identificación de materiales promisorios** para celdas solares mediante aprendizaje automático.

---

# 📁 Estructura del Repositorio

/
│── README.md ← Este archivo
│── perovskitas_filtradas_20251125_162228.csv
│── Script para generar tu propio dataset.txt
│── eficiencia_optimizada.ipynb



### **Descripción de cada archivo:**

### 📌 `perovskitas_filtradas_20251125_162228.csv`
Dataset real obtenido mediante la API del Materials Project.  
Incluye para cada material:

- **Material_ID**
- **Formula**
- **Band_Gap_eV**
- **Densidad_g_cm3**
- **Energia_Formacion_eatoms**
- **Es_Estable**
- **Es_Perovskita**
- **Structure_JSON**

Este archivo sirve como **fuente principal** para el modelado y análisis.

---

### 📌 `Script para generar tu propio dataset.txt`
Script totalmente funcional para permitir a cualquier usuario:

1. Conectarse al **Materials Project** usando `mp-api`
2. Descargar materiales estables
3. Filtrar por band gap óptimo (1.0 – 1.8 eV)
4. Identificar posibles perovskitas
5. Exportar un archivo `.csv` listo para usar

🏷 **Nota:**  
Debes reemplazar `TU_KEY_API_REAL` con tu clave del Materials Project.

---

### 📌 `eficiencia_optimizada.ipynb`
Notebook principal del proyecto. Contiene:

- Exploración del dataset  
- Feature engineering  
- Entrenamiento de Random Forest y XGBoost  
- Comparación de métricas (MAE, RMSE, R²)  
- Importancia de variables  
- Predicciones del ensemble  
- Ranking final de candidatos a mejor eficiencia teórica  

Este notebook es **totalmente reproducible** y explica cada paso del pipeline.

---

# 🎯 Objetivos del Proyecto

### ✔ Predicción de Band Gap usando ML  
Entrenamos modelos capaces de anticipar el band gap de nuevos materiales basándose en sus propiedades estructurales y termodinámicas.

### ✔ Priorización de materiales promisorios  
Se genera un ranking con los candidatos más cercanos al **band gap ideal (1.34 eV)** para celdas solares de alta eficiencia.

### ✔ Feature Engineering orientado a ciencia de materiales  
Incluye descriptores relacionados con:

- estabilidad
- densidad
- energía de formación
- características composicionales

---

# 🧪 Modelos Utilizados

- **Random Forest Regressor**
- **XGBoost Regressor**
- **Regresión Lineal** (baseline simple)

Cada uno se evalúa con:

- **MAE**  
- **RMSE**  
- **R²**

El ensemble final combina RF + XGB ponderados según su desempeño real.

---

# 📊 Resultados Principales

- Comparación de modelos (MAE / RMSE / R²)
- Importancia de características
- Gráfico de dispersión Real vs Predicho
- Ranking **Top–15 materiales candidatos**

Todos estos resultados pueden reproducirse ejecutando:

> `eficiencia_optimizada.ipynb`

---

# ⚙️ Cómo Ejecutar el Notebook

### 1️⃣ Instalar dependencias

pip install pandas scikit-learn xgboost matplotlib mp-api
2️⃣ (Opcional) Generar tu propio dataset
Abrir Script para generar tu propio dataset.txt y:

colocar tu MP_API_KEY

ejecutar el script en Python

3️⃣ Correr el notebook
Abrir:


eficiencia_optimizada.ipynb
y ejecutar todas las celdas.

🧠 Fuente de Datos
Este proyecto utiliza datos del:

Materials Project (MP)
🔗 https://materialsproject.org

Agradecimientos a MP por su API pública y sus datos estructurales / electrónicos computados mediante DFT.

📄 Licencia

No incluye claves privadas ni accesos al MP.

📞 Contacto
Si quieres mejorar este proyecto, extenderlo, o colaborar:

Sneider Rincon C

Castrillon

LinkedIn:https://www.linkedin.com/in/sneider-rincon/

🌞 Contribución
Pull requests, issues y sugerencias son bienvenidas.

Este repositorio busca apoyar la conexión entre:

📌 Ciencia de Materiales + 📌 Computación Científica + 📌 Inteligencia Artificial


