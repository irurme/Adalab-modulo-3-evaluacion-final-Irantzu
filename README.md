# ✈️ Análisis de Vuelos y Clientes: Programa de Lealtad de Aerolínea

Este repositorio contiene el ejercicio de evaluación final del **Módulo 3: Data Analysis**. El objetivo principal es explorar, limpiar y analizar datos relacionados con el comportamiento de clientes dentro de un programa de lealtad de una aerolínea, para extraer conocimientos clave sobre sus patrones de vuelo y perfiles demográficos.

## 📊 Los Datos

El análisis se basa en dos conjuntos de datos CSV que describen la actividad de vuelo y el perfil de los clientes:

### `Customer Flight Analysis.csv`

Este archivo detalla la actividad de vuelo de los clientes en un programa de lealtad.

* **Loyalty Number:** Identificador único del cliente.
* **Year:** Año de la actividad de vuelo.
* **Month:** Mes de la actividad de vuelo (1-12).
* **Flights Booked:** Número total de vuelos reservados por el cliente en ese mes.
* **Flights with Companions:** Número de vuelos reservados en los cuales el cliente viajó con acompañantes.
* **Total Flights:** El número total de vuelos que el cliente ha realizado, que puede incluir vuelos reservados en meses anteriores.
* **Distance:** La distancia total (presumiblemente en millas o kilómetros) que el cliente ha volado durante el mes.
* **Points Accumulated:** Puntos acumulados por el cliente en el programa de lealtad durante el mes, con base en la distancia volada u otros factores.
* **Points Redeemed:** Puntos que el cliente ha redimido en el mes, posiblemente para obtener beneficios como vuelos gratis, mejoras, etc.
* **Dollar Cost Points Redeemed:** El valor en dólares de los puntos que el cliente ha redimido durante el mes.

### `Customer Loyalty History.csv`

Este archivo proporciona un perfil detallado de cada cliente.

* **Loyalty Number:** Identificador único del cliente (clave para unir con el archivo de vuelos).
* **Country:** País de residencia.
* **Province:** Provincia o estado de residencia.
* **City:** Ciudad de residencia.
* **Postal Code:** Código postal.
* **Gender:** Género del cliente.
* **Education:** Nivel educativo alcanzado.
* **Salary:** Ingreso anual estimado.
* **Marital Status:** Estado civil.
* **Loyalty Card:** Tipo de tarjeta de lealtad que posee el cliente. Esto podría indicar distintos niveles o categorías dentro del programa de lealtad.
* **CLV (Customer Lifetime Value):** Valor total estimado que el cliente aporta a la empresa durante toda la relación que mantiene con ella.
* **Enrollment Type:** Tipo de inscripción del cliente en el programa de lealtad (ej. Standard).
* **Enrollment Year:** Año en que el cliente se inscribió en el programa de lealtad.
* **Enrollment Month:** Mes en que el cliente se inscribió en el programa de lealtad.
* **Cancellation Year:** Año en que el cliente canceló su membresía en el programa de lealtad, si aplica.
* **Cancellation Month:** Mes en que el cliente canceló su membresía en el programa de lealtad, si aplica.

## 🚀 Fases del Ejercicio

El ejercicio se estructura en tres fases principales:

### Fase 1: Exploración y Limpieza

Esta fase se centra en preparar los datos para el análisis.

* **1.1. Exploración Inicial:**
    * Identificar posibles problemas (nulos, atípicos).
    * Usar funciones de Pandas para entender la estructura y el estado de los datos.
    * Unir los dos conjuntos de datos (`Customer Flight Analysis.csv` y `Customer Loyalty History.csv`).
* **1.2. Limpieza de Datos:**
    * Eliminar o tratar valores nulos en columnas clave.
    * Verificar y asegurar la consistencia y corrección de los datos.
    * Realizar ajustes o conversiones de tipos de datos.

### Fase 2: Visualización

En esta fase, se utilizarán herramientas de visualización (Seaborn, Matplotlib) para responder a las siguientes preguntas clave, eligiendo el gráfico más adecuado para cada una:

* **2.1. Distribución de Vuelos Reservados por Mes:** ¿Cómo se distribuye la cantidad de vuelos reservados por mes durante el año?
* **2.2. Relación Distancia vs. Puntos Acumulados:** ¿Existe una relación entre la distancia de los vuelos y los puntos acumulados por los clientes?
* **2.3. Distribución de Clientes por Provincia/Estado:** ¿Cuál es la distribución de los clientes por provincia o estado?
* **2.4. Salario Promedio vs. Nivel Educativo:** ¿Cómo se compara el salario promedio entre los diferentes niveles educativos de los clientes?
* **2.5. Proporción de Clientes por Tipo de Tarjeta de Fidelidad:** ¿Cuál es la proporción de clientes con diferentes tipos de tarjetas de fidelidad?
* **2.6. Distribución de Clientes por Estado Civil y Género:** ¿Cómo se distribuyen los clientes según su estado civil y género?

### Fase 3: Evaluación de Diferencias en Reservas de Vuelos por Nivel Educativo (BONUS)

Esta fase profundiza en el análisis estadístico para determinar si el nivel educativo influye significativamente en el número de vuelos reservados.

* **3.1. Preparación de Datos:**
    * Filtrar el conjunto de datos para incluir únicamente las columnas relevantes: `'Flights Booked'` y `'Education'`.
* **3.2. Análisis Descriptivo:**
    * Agrupar los datos por nivel educativo y calcular estadísticas descriptivas básicas (como el promedio, la desviación estándar, la mediana, etc.) del número de vuelos reservados para cada grupo.
* **3.3. Prueba Estadística:**
    * Realizar una prueba de hipótesis adecuada para determinar si existe una diferencia estadísticamente significativa en el número de vuelos reservados entre los diferentes niveles educativos.

## 🛠️ Tecnologías Utilizadas

* **Python**
* **Pandas:** Manipulación y análisis de datos.
* **Matplotlib:** Creación de gráficos.
* **Seaborn:** Visualizaciones estadísticas avanzadas y estéticas.
* **NumPy:** Operaciones numéricas.
* **SciPy (stats):** Para pruebas estadísticas.

## 👩‍💻 Autora

- **Nombre**: Irantzu Urkiola 
- **Curso**: Adalab - Data Analyst (promor 52 - Julia Salander)
- **Módulo**: 3 - Python - Transformando datos
