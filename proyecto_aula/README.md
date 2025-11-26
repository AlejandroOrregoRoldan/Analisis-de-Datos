# **Análisis Exploratorio de Factores de Éxito en Campañas de Marketing Bancario**

---

### **Autor**
* Alejandro Orrego Roldán

---

## **Objetivo del Proyecto**
Realizar un ciclo completo de ciencia de datos, desde el análisis exploratorio (EDA) hasta el preprocesamiento, para identificar los predictores clave de éxito en la suscripción de depósitos a plazo fijo y preparar los datos para futuros modelos de Inteligencia Artificial.

---

## **Estructura del Proyecto**

Esta carpeta contiene el desarrollo técnico del proyecto, organizado de la siguiente manera:

* **`/data`**: Contiene los datasets en sus diferentes etapas de evolución.
    * `bank.csv`: El dataset original sin procesar.
    * `bank_depurado.csv`: El dataset limpio, con los valores "unknown" de `job` y `education` ya tratados.
    * `bank_preprocesado.csv`: El dataset final, con variables categóricas codificadas (encoding) y numéricas escaladas, listo para algoritmos de ML.

* **Notebooks de Análisis:**
    * **`Analisis_Marketing_Bancario.ipynb`**: (Fase 1) Contiene el Análisis Exploratorio de Datos (EDA).
        1. Carga y limpieza de datos.
        2. Análisis y manejo de valores "unknown".
        3. Análisis Univariado, Bivariado y Multivariado.
        4. Detección de atípicos (Outliers).
        5. Conclusiones del negocio.

    * **`Preprocesamiento_Datos_Bancarios.ipynb`**: (Fase 2) Contiene la Ingeniería de Características (Unidad 4).
        1. Carga del dataset depurado.
        2. Codificación de variables categóricas (One-Hot Encoding y Label Encoding).
        3. Escalamiento de variables numéricas (MinMax Scaling).
        4. Exportación del dataset final.

* **`README.md`**: Este archivo. Documentación técnica del contenido de la carpeta.

---

## **Diccionario de Variables Utilizadas**

A continuación se describen las variables analizadas y transformadas durante el proyecto:

| Nombre de la Variable | Tipo (Original) | Definición |
| :--- | :--- | :--- |
| `age` | Continua | La edad del cliente en años. |
| `job` | Discreta | El tipo de trabajo u ocupación del cliente. |
| `marital` | Discreta | El estado civil del cliente (ej. 'married', 'single'). |
| `education` | Discreta | El nivel educativo más alto alcanzado. |
| `default` | Discreta | Indica si el cliente tiene crédito en mora. |
| `balance` | Continua | El saldo promedio anual del cliente en euros. |
| `housing` | Discreta | Indica si tiene préstamo de vivienda. |
| `loan` | Discreta | Indica si tiene préstamo personal. |
| `contact` | Discreta | Método de comunicación (ej. 'cellular'). |
| `day` | Discreta | Día del mes del último contacto. |
| `month` | Discreta | Mes del año del último contacto. |
| `duration` | Continua | Duración del último contacto en segundos. |
| `campaign` | Continua | Número de contactos realizados durante esta campaña. |
| `pdays` | Continua | Días desde el último contacto previo (-1 si es nuevo). |
| `previous` | Continua | Número de contactos previos antes de esta campaña. |
| `poutcome` | Discreta | Resultado de la campaña de marketing anterior. |
| `deposit` | Discreta | **Variable Objetivo:** ¿El cliente se suscribió? ('yes'/'no'). |