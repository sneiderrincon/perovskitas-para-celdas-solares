# 🔬 Predicción de Materiales Fotovoltaicos con Machine Learning  
### Ensemble Learning y Análisis Estructural de Perovskitas usando datos reales del Materials Project

Este repositorio contiene un **pipeline científico completo** para la **identificación y priorización de materiales fotovoltaicos tipo perovskita**, combinando:

- 📊 Datos reales del **Materials Project**
- 🧠 Modelos de **Machine Learning**
- 🧪 Análisis **estructural y termodinámico**
- ⚙️ Automatización de datasets
- 📈 Ranking de materiales candidatos para celdas solares

El objetivo es **acelerar el descubrimiento de materiales promisorios** para aplicaciones fotovoltaicas, integrando **ciencia de materiales + inteligencia artificial**.

---

## 📁 Estructura del Repositorio

/
│── data/ # Datasets procesados y finales
│── json/ # Estructuras cristalinas en formato JSON (Materials Project)
│── images/ # Gráficos y visualizaciones
│── cif/ # Archivos CIF de estructuras cristalinas
│── models-pkl/ # Modelos entrenados serializados (.pkl)
│── notebooks/ # Notebooks de análisis y modelado
│── script-generar-data-set/ # Scripts para descarga y filtrado de datos
│── README.md # Documentación del proyecto


---

## 🧪 Descripción de Carpetas

### 📂 `data/`
Contiene los datasets finales utilizados para el entrenamiento y evaluación de modelos, incluyendo:

- Material ID
- Fórmula química
- Band Gap (eV)
- Energía de formación
- Densidad
- Estabilidad termodinámica
- Indicador de perovskita

---

### 📂 `json/`
Estructuras cristalinas completas descargadas desde el **Materials Project** en formato JSON.  
Estas estructuras se usan para:

- Análisis estructural
- Conversión a CIF
- Feature engineering basado en la red cristalina

---

### 📂 `cif/`
Archivos **CIF** generados a partir de las estructuras JSON.  
Permiten:

- Visualización cristalográfica
- Validación estructural
- Uso en software externo (VESTA, Materials Studio, etc.)

---

### 📂 `script-generar-data-set/`
Scripts automatizados que permiten:

1. Conectarse al **Materials Project API**
2. Descargar materiales estables
3. Filtrar por **band gap óptimo (1.0 – 1.8 eV)**
4. Identificar estructuras tipo perovskita
5. Exportar datasets listos para ML

📌 **Nota:**  
Es necesario configurar tu propia `MP_API_KEY`.

---

### 📂 `notebooks/`
Notebooks principales del proyecto, donde se desarrolla todo el pipeline:

- Exploración y limpieza de datos
- Feature engineering físico-químico
- Entrenamiento de modelos
- Evaluación comparativa
- Visualización de resultados
- Ranking final de materiales

---

### 📂 `models-pkl/`
Modelos entrenados y guardados en formato `.pkl`, incluyendo:

- Random Forest
- XGBoost
- Modelos ensemble

Permiten reutilización directa sin reentrenar.

---

## 🧠 Modelos de Machine Learning Utilizados

- **Random Forest Regressor**
- **XGBoost Regressor**
- **Regresión Lineal** (baseline)

### Métricas de evaluación:
- MAE
- RMSE
- R²

Se implementa un **ensemble ponderado** para mejorar la precisión en la predicción del **Band Gap**.

---

## 🎯 Objetivos del Proyecto

✔ Predicción precisa del **Band Gap**  
✔ Priorización de materiales cercanos al valor ideal (~1.34 eV)  
✔ Integración de propiedades estructurales y termodinámicas  
✔ Automatización del pipeline científico  
✔ Soporte a investigación en celdas solares

---

## ⚙️ Reproducción del Proyecto

### 1️⃣ Instalar dependencias
```bash
pip install pandas numpy scikit-learn xgboost matplotlib mp-api pymatgen
🧪 Fuente de Datos

Datos obtenidos desde:

Materials Project
🔗 https://materialsproject.org

Agradecimientos al MP por su API pública y datos computados mediante DFT.

📄 Licencia

Este repositorio no incluye claves privadas ni credenciales sensibles.
Uso académico y educativo.

📞 Contacto

Sneider Rincón C.
📍 Castrillón
🔗 LinkedIn: https://www.linkedin.com/in/sneider-rincon/

🌞 Contribuciones

Pull requests, issues y sugerencias son bienvenidas.

Este proyecto busca fortalecer la conexión entre:

📌 Ciencia de Materiales
📌 Computación Científica
📌 Inteligencia Artificial
