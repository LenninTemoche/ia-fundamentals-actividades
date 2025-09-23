## IA Fundamentals - Actividades
Repositorio para actividades del curso IA Fundamentals de IBM y Guayerd 2025

---

### Actividad 1: Crear repositorio y subir excel a github

Se creó este repositorio y se subió archivo csv “german_credit_data_biased_training.csv

- Add file (Agregar archivo).

- Upload files (Cargar archivos).

- Add files via upload (Agregar archivos mediante carga).

- Commit changes (Confirmar cambios).
  
---
---
### Actividad 2: Actividad Guiada en IBM Watson


## 🚗 Análisis de Fraude en Seguros con IBM Watson Studio

### Objetivo del Proyecto

Detectar reclamaciones fraudulentas en seguros de automóviles mediante análisis de datos, limpieza, visualización y validación de hipótesis en **IBM Watson Studio**.

> **Hipótesis de negocio:** “Las reclamaciones superiores a \$10,000 pueden ser fraudulentas.”



## Pasos Generales del Proyecto

### 1️⃣ Provisión del Servicio

* Inicia sesión en [IBM Cloud](https://cloud.ibm.com).
* Busca **IBM Watson Studio** en el catálogo y crea una instancia con el plan **Lite (gratuito)**.
* Lanza Watson Studio para acceder al entorno.

### 2️⃣ Crear un Proyecto Nuevo

* En Watson Studio, crea un nuevo **proyecto de análisis**.
* Asigna nombre, selecciona almacenamiento y confirma.

### 3️⃣ Importar el Dataset

* Sube el archivo `AutoInsClaims.csv` desde tu equipo. También puedes utilizar un dataset similar.
* Asegúrate de que aparezca en la sección de activos del proyecto.

### 4️⃣ Limpiar y Preparar los Datos

* Abre el dataset en **Data Refinery**.
* Elimina columnas irrelevantes (identificadores, vacías).
* Corrige tipos de datos (especialmente fechas).
* Guarda los cambios generando un nuevo archivo limpio (`AutoInsClaims_shaped.csv`).

### 5️⃣ Crear Variable Derivada para la Hipótesis

* Abre el archivo limpio y crea una nueva columna:

  * `EXCESSIVE_CLAIM_AMOUNT = 1` si el monto > \$10,000, `0` en caso contrario.
* Convierte la nueva columna a tipo entero (0/1).
* Guarda los cambios en un nuevo archivo (`reclamaciones_shaped_refined.csv`).

### 6️⃣ Visualizar para Validar la Hipótesis

* Abre el dataset refinado y crea un **gráfico de dispersión**:

  * Eje X: `EXCESSIVE_CLAIM_AMOUNT`
  * Eje Y: `CLAIM_AMOUNT`
  * Color: `FLAG_FOR_FRAUD_INV`
* Observa patrones de fraude y valida (o ajusta) la hipótesis.

### 7️⃣ Comunicar Insights

* Resume los hallazgos para una presentación ejecutiva.
* Destaca:

  * Alta concentración de fraude en montos altos.
  * Presencia de fraude también en montos bajos.
  * Importancia de no usar reglas simples, sino modelos predictivos.



## 📌 Recomendaciones

* Usar capturas de pantalla en cada paso para documentar el proceso.
* Guardar las visualizaciones en el proyecto.
* Considera usar **AutoAI** para entrenar un modelo predictivo en la siguiente fase.



## Archivos Generados

* `AutoInsClaims.csv` → original
* `AutoInsClaims_shaped.csv` → limpio
* `AutoInsClaims_shaped_shaped.csv` → con variable derivada
* `Visualización - Fraude vs. Monto Excesivo` → gráfico guardado



## 💡 Conclusión

Este proyecto no solo demuestra el uso técnico de Watson Studio, sino también la capacidad de **traducir datos en decisiones de negocio**, validando hipótesis con evidencia y comunicación efectiva.

---
---
## 🔮 Actividad 2.1 : Fase de Predicción generada en Python  Actividad Guiada IBM

En esta fase se desarrolló un **modelo predictivo de fraude** utilizando **Random Forest**. 

 * Archivo : Proyecto_Fraude_Seguros.ipynb

Se consideraron como variables clave:

- `EXCESSIVE_CLAIM_AMOUNT` (reclamos > $10,000)  
- `POLICE_REPORT`  
- `INCIDENT_CAUSE`  
- Diferencia temporal entre `LOSS_EVENT_TIME` y `CLAIM_INIT_TIME`  

### 📊 Resultados
- **Accuracy general:** 94%  
- **F1-score:** 0.94 (equilibrio entre precisión y recall)  
- El modelo clasifica correctamente la mayoría de reclamos legítimos y fraudulentos.  
- Se detecta una ligera tendencia a **perder algunos fraudes de bajo monto** (falsos negativos), aunque en número reducido.  

### ✅ Conclusión
El modelo es **altamente confiable** como sistema de apoyo para la detección de fraudes, reduciendo riesgos financieros y falsos positivos.  
Se recomienda ajustarlo como **herramienta de alerta temprana**, acompañada de revisión manual en casos sospechosos.


---
---


