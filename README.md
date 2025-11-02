## Análisis de Precios de Airbnb en Madrid

---

## 📋 Descripción del Proyecto

Este proyecto consiste en un dashboard interactivo desarrollado en **Power BI** para analizar los datos de alojamientos de Airbnb en Madrid. El objetivo es obtener insights relevantes sobre los precios, distribución geográfica, tipos de propiedades y patrones de actividad en la plataforma.

---

## 🎯 Objetivos del Análisis

- Analizar la distribución de precios por barrio y tipo de alojamiento
- Identificar patrones geográficos en la concentración de alojamientos
- Evaluar la relación entre precio, tipo de propiedad y características del alojamiento
- Medir la actividad y popularidad de los alojamientos mediante reviews
- Proporcionar KPIs relevantes para la toma de decisiones

---

## 📁 Fuente de Datos

**Dataset:** `airbnb-listings Madrid.csv`

**Columnas principales utilizadas:**
- **Identificación:** id, name, host_id, host_name
- **Ubicación:** neighbourhood_cleansed, latitude, longitude
- **Tipo:** property_type, room_type
- **Capacidad:** accommodates, bedrooms, beds, bathrooms
- **Precio:** price
- **Disponibilidad:** availability_365
- **Reviews:** number_of_reviews, reviews_per_month, review_scores_rating
- **Fechas:** last_scraped, host_since, first_review, last_review

**Total de registros analizados:** 13,227 alojamientos en Madrid

---

## 📊 Estructura del Dashboard

El dashboard está compuesto por **4 páginas interactivas:**

---

### 📄 Página 1: Overview (Vista General)

**Título:** "Análisis de Precios - Airbnb Madrid"

**Objetivo:** Proporcionar una visión general de los KPIs principales y la distribución de alojamientos.

**KPIs Principales:**
- **Total Alojamientos:** 13,227
- **Precio Promedio:** 65.89€
- **Precio Mediano:** 52.00€
- **Alojamientos Activos:** 11,000+

**Visualizaciones:**

1. **4 Tarjetas KPI:**
   - Total Alojamientos: 13,227
   - Precio Promedio: 65.89€
   - Precio Mediano: 52.00€
   - Alojamientos Activos: 11K

2. **Gráfico de Donut:**
   - Distribución por Room Type:
     - Entire home/apt: 59.81% (7,911 alojamientos)
     - Private room: 38.75% (5,125 alojamientos)
     - Shared room: 1.44% (191 alojamientos)
   - Tooltip: Precio Promedio

3. **Gráfico de Barras Horizontales:**
   - Top 10 Property Types por Total Alojamientos
   - Apartment domina con >10K alojamientos
   - Formato condicional por precio

4. **Tabla Resumen:**
   - Room Type con estadísticas completas:
     - Entire home/apt: 7,911 alojamientos, 87.27€ promedio
     - Private room: 5,125 alojamientos, 34.24€ promedio
     - Shared room: 191 alojamientos, 29.85€ promedio
   - Columnas: Total Alojamientos, Precio Promedio, Precio Mediano, P25 Precio, P75 Precio

**Filtros (Slicers):**
- Neighbourhood Cleansed (desplegable)
- Rango Precio (lista con checkboxes)

**Interactividad:** Cross-filtering entre todos los visuales

---

### 🗺️ Página 2: Análisis Geográfico

**Título:** "Análisis de Precios por Barrio"

**Objetivo:** Analizar la distribución de precios por barrio y ubicación geográfica.

**Visualizaciones:**

1. **Gráfico de Barras Horizontales (Principal):**
   - Barrios ordenados por Precio Promedio
   - Formato condicional con gradiente: Verde (económico) → Rojo (caro)
   - **Barrios más caros:** El Plantío (280€), Palomas, Recoletos
   - **Barrios más económicos:** Almagro, Justicia, Palacio

2. **Tabla Detallada:**
   - Lista completa de barrios con:
     - Neighbourhood Cleansed
     - Total Alojamientos (Total: 13,227)
     - Precio Promedio (Promedio general: 65.89€)
     - Precio Mediano (Mediana general: 52.00€)
     - % Diferencia vs Promedio (con formato condicional)

3. **Scatter Chart (Distribución Geográfica):**
   - X-axis: Longitude
   - Y-axis: Latitude
   - Size: Total Alojamientos
   - Legend: Room Type
   - Muestra concentración geográfica de alojamientos en Madrid
   - Los círculos más grandes indican mayor concentración de alojamientos

**Filtros:**
- Neighbourhood Cleansed
- Total Alojamientos
- Precio Promedio
- Precio Mediano

---

### 🔍 Página 3: Análisis Detallado

**Título:** "Análisis Detallado de Precios"

**Objetivo:** Análisis profundo con jerarquías y comparaciones múltiples.

**Visualizaciones:**

1. **Matriz con Jerarquía (Principal):**
   - Rows: Neighbourhood Cleansed > Property Type (expandible)
   - Values: Total Alojamientos (13,227 total), Precio Promedio (65.89€), Precio Mínimo (9.00€), Precio Máximo (870€)
   - Formato condicional en columna de Precio Promedio (gradiente verde-rojo)
   - Permite explorar precios por barrio y dentro de cada barrio por tipo de propiedad

2. **Gráfico de Barras Apiladas:**
   - Top barrios por Total Alojamientos
   - Apilado por Room Type (Entire home/apt, Private room, Shared room)
   - Muestra la composición de tipos de alojamiento por barrio
   - Embajadores, Universidad y Palacio lideran en cantidad

3. **Scatter Chart:**
   - X-axis: Average of Number of Reviews
   - Y-axis: Average of Price
   - Size: Average of Accommodates
   - Legend: Room Type
   - Analiza la relación entre popularidad (reviews) y precio
   - Muestra que no hay correlación directa entre cantidad de reviews y precio

**Filtros:**
- % Diferencia vs Promedio
- Neighbourhood Cleansed
- Precio Mediano
- Precio Promedio
- Total Alojamientos
- Property Type (slicer)
- Bedrooms (slider numérico de 0-10)

---

### 📈 Página 4: Actividad y Reviews

**Título:** "Análisis de Actividad y Popularidad"

**Objetivo:** Medir la actividad, popularidad y distribución de precios.

**KPIs Principales:**
- **Reviews por Mes:** 167.56
- **Alojamientos Activos:** 11K
- **Tasa Ocupación Estimada:** 0.44 (44%)
- **Índice Popularidad:** 68.50K

**Visualizaciones:**

1. **4 Tarjetas KPI:**
   - Reviews por Mes: 167.56
   - Alojamientos Activos: 11K
   - Tasa Ocupación Estimada: 0.44
   - Índice Popularidad: 68.50K

2. **Histograma de Precios:**
   - Distribución de alojamientos por rangos de precio (bins de 25€)
   - Muestra alta concentración en el rango 25-100€
   - La mayoría de alojamientos están por debajo de 200€
   - Pocos alojamientos superan los 500€

3. **Gráfico de Barras Combinado:**
   - Comparación de Precio Promedio (azul claro) y Reviews por Mes (azul oscuro) por Room Type
   - Entire home/apt: Mayor precio (~90€) y reviews (~170/mes)
   - Private room: Precio moderado (~40€) y reviews altas (~150/mes)
   - Shared room: Precio más bajo (~30€) y reviews moderadas (~110/mes)

4. **Gráfico de Donut:**
   - Distribución porcentual por Room Type
   - Entire home/apt: 0K (1.44%) - Shared room
   - 5K (38.75%) - Private room
   - 8K (59.81%) - Entire home/apt

5. **2 Gauge Charts (Velocímetros):**
   - Tasa Ocupación Estimada: 0.44 (escala 0.00-0.87)
   - Reviews por Mes: 167.56 (escala 0.00-335.12)

**Filtros:**
- Room Type (checkboxes)
- Neighbourhood Cleansed (desplegable)

---

## 🔄 Interactividad Implementada

### Cross-Filtering (Filtrado Cruzado):

Todos los visuales en cada página están conectados mediante cross-filtering:
- Al hacer clic en cualquier elemento (barra, porción de gráfico, fila de tabla), todos los demás visuales se filtran automáticamente
- Permite exploración dinámica de los datos
- Ejemplo: Al seleccionar "Entire home/apt" en el donut, todos los visuales muestran solo datos de ese tipo

### Slicers (Filtros):

- **Neighbourhood Cleansed:** Permite filtrar por barrio específico
- **Room Type:** Filtra por tipo de habitación (checkboxes múltiples)
- **Rango Precio:** Filtra por categoría de precio (Económico, Moderado, Premium, Lujo)
- **Property Type:** Filtra por tipo de propiedad
- **Bedrooms:** Slider numérico para filtrar por número de habitaciones (0-10)

### Tooltips:

Tooltips personalizados en todos los visuales principales con información adicional contextual sobre precios, cantidad de alojamientos y características.

---

## 📊 Insights Principales Obtenidos

### Distribución de Precios:

- **Precio promedio general:** 65.89€ por noche
- **Precio mediano:** 52.00€ (indica distribución asimétrica con valores altos que elevan el promedio)
- **Rango de precios:** Desde 9.00€ hasta 870.00€
- **Concentración:** La mayoría de alojamientos (>70%) están en el rango 25-100€
- **P25:** 31.00€ | **P75:** 80.00€

### Por Tipo de Alojamiento (Room Type):

- **Entire home/apt:** 
  - 59.81% del total (7,911 alojamientos)
  - Precio promedio: 87.27€
  - Precio mediano: 71.00€
  
- **Private room:** 
  - 38.75% del total (5,125 alojamientos)
  - Precio promedio: 34.24€
  - Precio mediano: 29.00€
  
- **Shared room:** 
  - 1.44% del total (191 alojamientos)
  - Precio promedio: 29.85€
  - Precio mediano: 19.00€

### Por Barrio (Neighbourhood):

- **Barrios más caros:** El Plantío (280€), Palomas, Recoletos, Fuentelarreina
- **Barrios más económicos:** Varios barrios periféricos con precios <30€
- **Mayor concentración de alojamientos:** Embajadores, Universidad, Palacio, Sol, Justicia
- **Variabilidad:** Alta dispersión de precios entre barrios (diferencias de hasta 250€)

### Por Tipo de Propiedad (Property Type):

- **Apartments dominan ampliamente:** >10,000 alojamientos
- **Otros tipos minoritarios:** House, Condominium, Bed & Breakfast, Loft, etc.
- **Total de tipos diferentes:** 10+ categorías de propiedades

### Actividad y Popularidad:

- **Alojamientos activos (con reviews):** ~11,000 de 13,227 (83%)
- **Reviews por mes promedio:** 167.56 (alta actividad)
- **Tasa de ocupación estimada:** 44% (moderada-alta)
- **Índice de popularidad:** 68,500
- **Correlación precio-reviews:** No se observa correlación directa; alojamientos económicos pueden tener muchas reviews

### Distribución Geográfica:

- **Concentración central:** Mayor densidad de alojamientos en el centro de Madrid
- **Dispersión:** Presencia en barrios periféricos pero con menor densidad
- **Hotspots:** Zonas con alta concentración visible en el scatter plot geográfico

---

## 🛠️ Tecnologías y Herramientas

- **Power BI Desktop** - Versión Desktop para creación del dashboard
- **Power Query** - Para transformación y limpieza de datos
- **DAX (Data Analysis Expressions)** - Para medidas calculadas y columnas
- **CSV** - Formato de datos de entrada
