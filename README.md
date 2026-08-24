# Google Cloud & BigQuery: Data Engineering Labs

## 🎯 Objetivo del Proyecto
Este repositorio contiene la implementación práctica de 12 laboratorios orientados a la ingeniería de datos y el análisis avanzado en Google Cloud Platform (GCP). El propósito de este proyecto es demostrar la capacidad para desplegar infraestructura como código, construir pipelines de datos eficientes, aplicar modelos de Machine Learning nativos y asegurar la gobernanza de la información.

## 🛠️ Stack Tecnológico
* **Cloud Computing:** Google Cloud Platform (BigQuery, Cloud Storage, Pub/Sub, Cloud SQL)
* **Infraestructura como Código (IaC):** Terraform
* **Transformación y Modelado:** dbt (Data Build Tool), SQL Avanzado
* **Integración Programática:** Python
* **CI/CD:** GitHub Actions

## 📂 Estructura del Repositorio
El código está organizado de forma modular, abarcando todo el ciclo de vida del dato:

* **`lab01-setup-inicial` a `lab03-external-tables`**: Despliegue de la infraestructura base, ingesta por lotes (Batch) desde Cloud Storage y configuración de consultas federadas sobre tablas externas.
* **`lab04-partitioning-clustering` a `lab05-advanced-sql`**: Estrategias de optimización de rendimiento y reducción de costes en BigQuery, junto con transformaciones analíticas complejas mediante Window Functions.
* **`lab06-bigquery-ml`**: Entrenamiento e implementación de modelos de Regresión Lineal utilizando el motor nativo de Machine Learning de BigQuery.
* **`lab07-security-governance`**: Implementación de políticas de seguridad, control de acceso a nivel de fila (Row-Level Security) y enmascaramiento dinámico de datos sensibles.
* **`lab08-streaming-pubsub` a `lab09-federated-queries`**: Creación de pipelines de ingesta en tiempo real orientados a eventos y conexión directa a bases de datos transaccionales (PostgreSQL).
* **`lab10-dbt-transformation` a `lab11-python-integration`**: Refinamiento y transformación de datos utilizando la arquitectura de dbt, e interacción programática con el entorno utilizando la librería cliente de Python.
* **`lab12-cicd-pipeline`**: Automatización de despliegues y validación de infraestructura mediante flujos de trabajo en GitHub Actions.

## 🚀 Instalación y Uso
Para desplegar estos laboratorios en tu propio entorno de GCP, es necesario contar con **Terraform** y el **Google Cloud SDK** instalados.

1. **Clonar el repositorio:**
   ```bash
   git clone https://github.com/hum1-ua/curso-gcp-bigquery.git
   cd curso-gcp-bigquery

2. **Autenticación en Google Cloud:**
   ```bash
   gcloud auth login
   gcloud config set project TU_PROJECT_ID
   gcloud auth application-default login

3. **Configuración del Proyecto en Terraform:**
Antes de desplegar la infraestructura de cualquier laboratorio, debes navegar a su respectiva carpeta terraform/ y modificar el archivo variables.tf.
Es imprescindible que sustituyas el valor asignado a la variable del ID del proyecto por el ID de tu propio proyecto en Google Cloud.

4. **Despliegue de un laboratorio específico (Ejemplo lab01):**
   ```bash
   cd lab01-setup-inicial/terraform
   terraform init
   terraform plan
   terraform apply -auto-approve

## 📚 Créditos y Referencias
Este repositorio ha sido desarrollado siguiendo el modelo de aprendizaje práctico estructurado en el curso integral de BigQuery impartido por el canal de YouTube *Google Cloud con Eduardo*. El código ha sido desplegado, documentado y probado como parte de mi formación técnica continua en ingeniería de datos y arquitectura en la nube.

* **Fuente original:** [Curso gratis de BIGQUERY desde CERO a Data Engineer | SQL y Python en Google Cloud](https://www.youtube.com/watch?v=XsUe5Ku-oac)
