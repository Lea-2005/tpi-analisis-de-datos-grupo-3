# Datos

## Origen
- **Dataset:** Telco Customer Churn
- **Fuente original:** IBM Sample Data Sets, publicado en [Kaggle](https://www.kaggle.com/datasets/blastchar/telco-customer-churn)
- **Copia usada por el notebook:** `https://raw.githubusercontent.com/IBM/telco-customer-churn-on-icp4d/master/data/Telco-Customer-Churn.csv`
- **Dimensiones:** 7.043 filas (clientes) × 21 columnas

El notebook descarga el archivo automáticamente, así que **no hace falta guardar el CSV en el repositorio**. Si se prefiere trabajar sin conexión, se puede descargar desde Kaggle y guardarlo en `data/raw/` como `WA_Fn-UseC_-Telco-Customer-Churn.csv`: el notebook lo detecta y lo usa.

Los `.csv` de `raw/` y `processed/` están excluidos en `.gitignore`. El dataset limpio (`processed/telco_churn_limpio.csv`) se genera al ejecutar el notebook.

## Diccionario de variables

| Variable | Descripción | Tipo |
|---|---|---|
| `customerID` | Identificador único del cliente | Cualitativa nominal (ID) |
| `gender` | Género (*Male* / *Female*) | Cualitativa nominal |
| `SeniorCitizen` | Adulto mayor (1) o no (0) | Cualitativa nominal |
| `Partner` | Tiene pareja | Cualitativa nominal |
| `Dependents` | Tiene personas a cargo | Cualitativa nominal |
| `tenure` | Antigüedad como cliente, en meses | Cuantitativa discreta |
| `PhoneService` | Tiene servicio telefónico | Cualitativa nominal |
| `MultipleLines` | Tiene múltiples líneas | Cualitativa nominal |
| `InternetService` | Tipo de internet (*DSL*, *Fiber optic*, *No*) | Cualitativa nominal |
| `OnlineSecurity` | Seguridad online | Cualitativa nominal |
| `OnlineBackup` | Backup online | Cualitativa nominal |
| `DeviceProtection` | Protección de dispositivos | Cualitativa nominal |
| `TechSupport` | Soporte técnico | Cualitativa nominal |
| `StreamingTV` | Streaming de TV | Cualitativa nominal |
| `StreamingMovies` | Streaming de películas | Cualitativa nominal |
| `Contract` | Tipo de contrato (*Month-to-month*, *One year*, *Two year*) | Cualitativa ordinal |
| `PaperlessBilling` | Factura electrónica | Cualitativa nominal |
| `PaymentMethod` | Medio de pago | Cualitativa nominal |
| `MonthlyCharges` | Cargo mensual (USD) | Cuantitativa continua |
| `TotalCharges` | Cargo total acumulado (USD) | Cuantitativa continua |
| `Churn` | Canceló el servicio en el último mes (**variable objetivo**) | Cualitativa nominal |
