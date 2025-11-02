
# 📊 Exploración y Visualización de Datos
## Análisis de Precios de Airbnb en Madrid

📋 Descripción del Proyecto
Este proyecto consiste en un dashboard interactivo desarrollado en Power BI para analizar los datos de alojamientos de Airbnb en Madrid. El objetivo es obtener insights relevantes sobre los precios, distribución geográfica, tipos de propiedades y patrones de actividad en la plataforma.

🎯 Objetivos del Análisis

Analizar la distribución de precios por barrio y tipo de alojamiento
Identificar patrones geográficos en la concentración de alojamientos
Evaluar la relación entre precio, tipo de propiedad y características del alojamiento
Medir la actividad y popularidad de los alojamientos mediante reviews
Proporcionar KPIs relevantes para la toma de decisiones


📁 Fuente de Datos
Dataset: airbnb-listings Madrid.csv

## 📊 Estructura del Dashboard

El dashboard está compuesto por **4 páginas interactivas:**

---

### 📄 Página 1: Overview (Vista General)

**Objetivo:** Proporcionar una visión general de los KPIs principales y la distribución de alojamientos.

**Visualizaciones:**

1. **4 Tarjetas KPI:**
   - Total Alojamientos: 14,780
   - Precio Promedio: 73.56€
   - Precio Mediano: 55.00€
   - Alojamientos Activos: 12,000+

2. **Gráfico de Donut:**
   - Distribución por Room Type (Entire home/apt, Private room, Shared room)
   - Tooltip: Precio Promedio

3. **Gráfico de Barras Horizontales:**
   - Top 10 Property Types por Total Alojamientos
   - Formato condicional por precio

4. **Tabla Resumen:**
   - Columnas: Room Type, Total Alojamientos, Precio Promedio, Precio Mediano, P25 Precio, P75 Precio

**Filtros (Slicers):**
- Neighbourhood Cleansed (desplegable)
- Rango Precio (lista con checkboxes)

**Interactividad:** Cross-filtering entre todos los visuales

---

### 🗺️ Página 2: Análisis Geográfico

**Objetivo:** Analizar la distribución de precios por barrio y ubicación geográfica.

**Visualizaciones:**

1. **Gráfico de Barras Horizontales (Principal):**
   - Top 15 barrios ordenados por Precio Promedio
   - Formato condicional con gradiente: Verde (económico) → Rojo (caro)

2. **Tabla Detallada:**
   - Neighbourhood Cleansed
   - Total Alojamientos
   - Precio Promedio
   - Precio Mediano
   - % Diferencia vs Promedio (con formato condicional)

3. **Scatter Chart (Distribución Geográfica):**
   - X-axis: Longitude
   - Y-axis: Latitude
   - Size: Total Alojamientos
   - Legend: Room Type
   - Simula un mapa geográfico con coordenadas

**Filtros:**
- Neighbourhood Cleansed
- Precio Mediano
- Precio Promedio
- Total Alojamientos

**Título:** "Análisis de Precios por Barrio"

---

### 🔍 Página 3: Análisis Detallado

**Objetivo:** Análisis profundo con jerarquías y comparaciones múltiples.

**Visualizaciones:**

1. **Matriz con Jerarquía (Principal):**
   - Rows: Neighbourhood Cleansed > Property Type (expandible)
   - Values: Total Alojamientos, Precio Promedio, Precio Mínimo, Precio Máximo
   - Formato condicional en múltiples columnas (gradiente verde-rojo)

2. **Gráfico de Barras Apiladas:**
   - Top 10 barrios por Total Alojamientos
   - Apilado por Room Type
   - Muestra la composición de tipos de alojamiento por barrio

3. **Scatter Chart:**
   - X-axis: Number of Reviews
   - Y-axis: Price
   - Size: Accommodates
   - Legend: Room Type
   - Analiza la relación entre popularidad (reviews) y precio

**Filtros:**
- % Diferencia vs Promedio
- Neighbourhood Cleansed
- Precio Mediano
- Precio Promedio
- Total Alojamientos
- Property Type (slicer)
- Bedrooms (slider numérico)

**Título:** "Análisis Detallado de Precios"

---

### 📈 Página 4: Actividad y Reviews

**Objetivo:** Medir la actividad, popularidad y distribución de precios.

**Visualizaciones:**

1. **4 Tarjetas KPI:**
   - Reviews por Mes: 162.96
   - Alojamientos Activos: 12K
   - Tasa Ocupación Estimada: 0.45
   - Índice Popularidad: 75,000K

2. **Histograma de Precios:**
   - Distribución de alojamientos por rangos de precio (bins de 25€)
   - Muestra la concentración de precios en el mercado

3. **Gráfico de Barras:**
   - Comparación de Precio Promedio y Reviews por Mes por Room Type

4. **Gráfico de Donut:**
   - Distribución porcentual por Room Type

5. **2 Gauge Charts (Velocímetros):**
   - Tasa Ocupación Estimada (0-1)
   - Reviews por Mes

**Filtros:**
- Neighbourhood Cleansed
- Room Type

**Título:** "Análisis de Actividad y Popularidad"

---

### Paleta de Colores:

- **Primario:** Azul (#0078D4)
- **Positivo:** Verde (#28A745)
- **Negativo:** Rojo (#DC3545)
- **Neutro:** Gris (#6C757D)
- **Gradientes:** Verde → Amarillo → Rojo para indicadores de precio

### Formato de Datos:

- **Precios:** Formato de moneda (€)
- **Porcentajes:** Formato de % con 2 decimales
- **Números grandes:** Separadores de miles
- **Fechas:** Formato dd/mm/yyyy

---

## 🔄 Interactividad Implementada

### Cross-Filtering (Filtrado Cruzado):

Todos los visuales en cada página están conectados mediante cross-filtering:
- Al hacer clic en cualquier elemento (barra, porción de gráfico, fila de tabla), todos los demás visuales se filtran automáticamente
- Permite exploración dinámica de los datos

### Slicers (Filtros):

- **Neighbourhood Cleansed:** Permite filtrar por barrio
- **Room Type:** Filtra por tipo de habitación
- **Rango Precio:** Filtra por categoría de precio
- **Property Type:** Filtra por tipo de propiedad
- **Bedrooms:** Slider numérico para filtrar por número de habitaciones

### Tooltips:

Tooltips personalizados en todos los visuales principales con información adicional contextual.

---

## 📊 Insights Principales Obtenidos

### Distribución de Precios:

- **Precio promedio:** 73.56€ por noche
- **Precio mediano:** 55.00€ (indica que la mayoría de alojamientos están por debajo del promedio)
- **Concentración:** La mayoría de alojamientos (>60%) están en el rango 25-100€

### Por Barrio:

- **Más caros:** Malibú, Central & Western, 78703
- **Más económicos:** Teatro District, Stereo, Andratx
- **Mayor concentración:** Barrios céntricos tienen más alojamientos pero precios variados

### Por Tipo de Alojamiento:

- **Entire home/apt:** 60.73% del total, precio promedio más alto
- **Private room:** 37.86% del total, precio moderado
- **Shared room:** 1.41% del total, precio más bajo
- **Property Type más común:** Apartments

### Actividad y Popularidad:

- **Alojamientos activos:** ~12,000 (con reviews)
- **Reviews por mes promedio:** 1.62
- **Tasa de ocupación estimada:** 45%
- **Correlación:** Los alojamientos con más reviews no necesariamente tienen precios más altos

---

## 🛠️ Tecnologías y Herramientas

- **Power BI Desktop** - Versión Desktop para creación del dashboard
- **Power Query** - Para transformación y limpieza de datos
- **DAX (Data Analysis Expressions)** - Para medidas calculadas y columnas
- **CSV** - Formato de datos de entrada

---

## 📝 Notas Adicionales

- Los mapas geográficos estándar de Power BI están deshabilitados en el entorno, por lo que se utilizó un scatter plot con coordenadas (Latitude/Longitude) como alternativa efectiva.

---

## 🎓 Aprendizajes Clave

1. **Transformación de datos** con Power Query
2. **Creación de medidas DAX avanzadas** con funciones de contexto
3. **Diseño de dashboards** siguiendo principios UX/UI
4. **Análisis exploratorio** de datos inmobiliarios
5. **Implementación de interactividad** mediante cross-filtering y slicers
6. **Uso de formatos condicionales** para destacar insights
7. **Creación de jerarquías** y análisis drill-down

---

# 📊 Exploración y Visualización de Datos
## Análisis de Precios de Airbnb en Madrid
