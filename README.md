#TelecomX – Análisis de Evasión de Clientes (Churn)

¿Se están yendo los clientes?  
Sí.
¿Podemos entender por qué?  
Lo intentaremos. Y para eso hacemos este análisis

---

##Objetivo del Proyecto

El objetivo de este proyecto es analizar la evasión de clientes (Churn) en TelecomX utilizando un enfoque exploratorio de datos (EDA).

Buscamos:

- Identificar patrones asociados al abandono.
- Detectar factores de riesgo.
- Proponer acciones estratégicas para reducir la evasión.
- Traducir datos en decisiones (no solo en gráficos bonitos).

---

##Dataset

- Fuente: JSON público vía GitHub.
- Cada fila representa un cliente activo o que canceló el servicio.
- Contiene información:
  - Demográfica
  - Contractual
  - Servicios contratados
  - Facturación

El archivo original viene con estructura anidada (sí, hubo que aplanarlo a la fuerza).

---

##Limpieza y Preparación de Datos

Durante el proceso se realizaron:

- Normalización del JSON.
- Tratamiento de valores vacíos en la variable **Churn**.
- Conversión de variables numéricas.
- Verificación de duplicados (spoiler: no había).
- Creación de variables derivadas:
  - `Cuentas_Diarias`
  - `Churn_bin`
  - `Total_Servicios`

El 3% de registros tenía valores faltantes en churn y fueron excluidos solo en análisis donde era necesario.

---

##Principales Hallazgos

Algunas cosas interesantes (y un poco preocupantes):

### 1. El contrato importa. Mucho.
Los clientes con contrato **Month-to-month** tienen una tasa de churn cercana al 43%.  
Los contratos largos prácticamente blindan la evasión.

### 2. El riesgo está en los primeros meses
La mayoría de los clientes que abandonan tienen baja antigüedad.  
El problema está en el onboarding. 

### 3. Precio alto = más riesgo
Los clientes que se van pagan, en promedio, más que los que se quedan.  
¿Valor percibido insuficiente? Probablemente.

### 4. Más servicios = más retención
Soporte técnico y seguridad online reducen significativamente la tasa de churn.

### 5. Fibra óptica = mayor expectativa, mayor churn
El segmento fibra óptica presenta una de las tasas más altas de evasión.

---

## Insights Clave

La evasión no depende de un solo factor.  
Se da cuando se combinan:

- Contratos flexibles
- Baja antigüedad
- Alta carga económica
- Pocos servicios complementarios

En otras palabras: clientes nuevos, pagando más, sin mucha vinculación.

---

## Recomendaciones Estratégicas

Basado en el análisis:

- Incentivar contratos anuales.
- Reforzar el onboarding en los primeros 3 meses.
- Promover bundles con soporte técnico.
- Revisar propuesta de valor en fibra óptica.
- Implementar modelo predictivo de churn.

---

## Tecnologías Utilizadas

- Python
- Pandas
- NumPy
- Matplotlib

---

## Próximos Pasos

- Construcción de modelo predictivo.
- Segmentación avanzada.
- Análisis de impacto financiero del churn.
- Dashboard interactivo.

---

## Sobre el Proyecto

Este proyecto forma parte de mi proceso de formación en análisis de datos y ciencia de datos.  
Feedback, sugerencias o mejoras son más que bienvenidas.

Si llegaste hasta acá… leiste mas que el promedio, felicitaciones!
