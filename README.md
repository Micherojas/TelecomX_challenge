# TelecomX_challenge
📌 Introducción
Este proyecto analiza los factores que contribuyen a la evasión de clientes (Churn) en la empresa TelecomX.
El churn es un problema crítico para las telecomunicaciones, ya que retener clientes existentes es más rentable que adquirir nuevos.
El objetivo es identificar patrones y causas del churn para proponer estrategias efectivas de retención.

📂 Datos
Fuente de datos: TelecomX_Data.json

Formato: JSON con columnas que contienen diccionarios anidados.

Número de registros: ~7,000 clientes.

🛠 Tecnologías utilizadas
Python 3

Google Colab

Pandas – Limpieza y manipulación de datos.

Matplotlib – Visualización de datos.

🧹 Limpieza y tratamiento de datos
Normalización de columnas anidadas en diccionarios.

Renombrado de columnas a minúsculas para consistencia.

Expansión de la columna account_charges en:

Monthly – cargo mensual.

Total – cargo total.

Creación de columna Cuentas_Diarias = Monthly / 30.

Filtrado de valores vacíos en la columna churn.

Validación de ausencia de valores nulos en columnas relevantes.

📊 Análisis exploratorio (EDA)
Se exploraron patrones entre el churn y diferentes variables:

Distribución de churn: 26.5% de los clientes han evadido.

Churn por tipo de contrato:

Mes a mes: 42.7%

1 año: 11.3%

2 años: 2.8%

Churn por método de pago:

Electronic check: 45.3%

Bank transfer (automatic): 16.7%

Credit card (automatic): 15.2%

Churn por tipo de servicio de internet:

Fiber optic: 41.9%

DSL: 19.0%

Sin internet: 7.4%

Churn por servicio de seguridad online:

Sin seguridad: 41.8%

Con seguridad: 14.6%

Costo mensual promedio:

Churn “Yes”: 74.44

Churn “No”: 61.27

Total gastado: clientes que permanecen tienden a gastar más.

💡 Conclusiones clave
El churn no es aleatorio, está ligado a características de cliente, contrato, servicios y pago.

Contratos cortos y pagos electrónicos tienen mayor riesgo de evasión.

El servicio de fibra óptica está asociado con mayor churn.

Los servicios de seguridad online reducen la evasión.

Clientes de alto gasto son más leales.

📌 Recomendaciones
Fidelización para contratos mes a mes → incentivar contratos más largos.

Mejorar la experiencia del pago electrónico.

Optimizar el servicio de fibra óptica.

Promover seguridad online con paquetes atractivos.

Reconocer clientes de alto gasto con beneficios exclusivos.

Análisis adicional para modelado predictivo de churn.

▶ Ejecución del notebook
Abre en Google Colab el archivo .ipynb.

Instala dependencias si es necesario:

python
Copiar
Editar
!pip install pandas matplotlib
Carga los datos:

python
Copiar
Editar
import pandas as pd
url = "https://raw.githubusercontent.com/alura-cursos/challenge2-data-science-LATAM/refs/heads/main/TelecomX_Data.json"
df = pd.read_json(url)
Ejecuta las celdas en orden para reproducir el análisis.

📜 Licencia
Este proyecto se distribuye bajo licencia de uso educativo.
