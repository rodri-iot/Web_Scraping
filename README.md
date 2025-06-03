# Web Scraping
# 📄 Documento de Requisitos de los Interesados
- **Proyecto:** Sistema de Monitoreo de Precios en Supermercados de Bolivia
- **BI Professional:** Rodrigo Jurgen Pinedo Nava
- **Client/Sponsor:** Proyecto personal con posibles alianzas institucionales a futuro

### Problema de negocio
En el actual contexto de crisis económica e inflación persistente en Bolivia, los consumidores enfrentan dificultades para identificar los precios más convenientes de productos esenciales en supermercados. Al mismo tiempo, las empresas productoras y los supermercados carecen de herramientas públicas que les permitan visualizar en tiempo real la evolución del mercado y los precios de la competencia. Este proyecto se propone abordar ambas problemáticas mediante la automatización del relevamiento de precios en línea y su posterior visualización dinámica.

### Stakeholders principales
- Ciudadanía consumidora: interesada en acceder a precios actualizados para optimizar sus decisiones de compra.
- Empresas productoras y distribuidoras: buscan monitorear la presencia y precios de sus productos en distintos supermercados.
- Supermercados: interesados en analizar su posicionamiento frente a la competencia y ajustar sus estrategias de precios.
- Periodistas de datos y organizaciones no gubernamentales: potenciales usuarios del conjunto de datos para análisis socioeconómicos.

### Uso previsto por los stakeholders
- Consumidores: acceden a gráficos o tablas que les permiten comparar precios y marcas de forma sencilla.
- Productores y competidores: utilizan dashboards privados o informes descargables con datos históricos y análisis comparativos.
- Supermercados: reciben reportes personalizados que muestran su evolución de precios y posicionamiento relativo.
- Analistas, periodistas o investigadores: descargan datasets estructurados para estudios externos y reportes públicos.

### Requerimientos principales
- Implementación de un sistema automatizado de scraping diario de precios a partir de sitios de ecommerce de supermercados seleccionados.
- Almacenamiento estructurado de los datos recolectados, incluyendo los siguientes metadatos: fecha, ciudad, supermercado, sucursal, marca, categoría, subcategoría, nombre del producto, identificador único del producto, precio y unidad.
- Desarrollo de un dashboard público, inicialmente con Looker Studio, orientado a la ciudadanía en general.
- Generación de informes comparativos descargables, organizados por producto y supermercado.
- Escalabilidad del sistema hacia una aplicación web o móvil en fases futuras del proyecto.
- Potencial monetización del servicio mediante accesos premium o suscripciones destinadas a empresas del rubro.

# 📄 Documento de Requisitos del Proyecto

### Propósito
El proyecto busca brindar a la ciudadanía boliviana una herramienta accesible para conocer los precios actualizados de productos esenciales en supermercados de las ciudades de La Paz, Cochabamba y Santa Cruz. En paralelo, se construirá una base de datos histórica que permitirá generar visualizaciones interactivas para distintos perfiles de usuarios, incluyendo consumidores, empresas productoras y cadenas de supermercados. Dada la coyuntura económica nacional, el proyecto se posiciona como una solución de transparencia de precios y monitoreo del mercado minorista.

### Dependencias clave
- Equipo de desarrollo: conformado actualmente por el analista BI responsable del proyecto, encargado del scraping, modelado de datos, y desarrollo del dashboard.
- Fuentes de datos: sitios web de ecommerce de supermercados seleccionados (ej. Hipermaxi, Tía, Fidalga, IC Norte).
- Herramientas: Python para scraping automatizado, Google Sheets para almacenamiento inicial, Looker Studio para visualización.
- Entregables esperados:
    - Scripts de scraping funcionales y automatizados.
    - Base de datos estructurada de precios históricos.
    - Dashboard público con visualizaciones clave por producto, ciudad y supermercado.
    - Informes descargables para empresas interesadas.
 
### Requisitos de los stakeholders
Basados en el Documento de Requisitos de los Interesados, los requerimientos han sido priorizados de la siguiente forma:

| Requisito                                                              | Prioridad |
| ---------------------------------------------------------------------- | --------- |
| Automatización diaria del scraping de precios                          | R         |
| Almacenamiento estructurado de datos históricos                        | R         |
| Dashboard público con filtros por ciudad, categoría y producto         | R         |
| Visualización de series temporales y comparaciones entre supermercados | R         |
| Posibilidad de exportar informes en formatos abiertos (CSV/PDF)        | D         |
| Dashboard privado para empresas productoras o supermercados            | D         |
| Acceso restringido para perfiles empresariales mediante login o token  | N         |
| Integración futura con apps móviles                                    | N         |

### Criterios de éxito
Se considerará exitoso este proyecto si se cumplen los siguientes indicadores SMART:

- Automatización diaria del scraping de al menos 3 supermercados por ciudad sin errores durante 30 días consecutivos.
- Almacenamiento correcto de más de 1.000 registros únicos de productos en un lapso de un mes.
- Publicación del dashboard funcional en Looker Studio con al menos tres visualizaciones interactivas: evolución de precios, comparativo por ciudad y ranking de supermercados.
- Acceso público al dashboard validado por al menos 100 usuarios únicos en su primer mes de lanzamiento.

### Recorrido del usuario (User journeys)

**Experiencia actual:**

Los consumidores deben visitar múltiples sitios web manualmente para buscar precios, sin garantías de actualización ni posibilidad de comparar entre supermercados o ciudades. Las empresas productoras no cuentan con herramientas para auditar precios públicos de sus productos ni analizar el mercado minorista con datos abiertos.

**Experiencia futura ideal:**

Los usuarios acceden a una plataforma que centraliza la información de precios, les permite comparar, visualizar tendencias y descargar información útil. Las empresas pueden explorar reportes históricos y tomar decisiones informadas sobre pricing y posicionamiento.

### Supuestos
- Las páginas de ecommerce de supermercados seguirán siendo accesibles públicamente sin necesidad de autenticación.
- Los productos mantienen estructuras HTML reconocibles para los scrapers durante la duración del proyecto.
- Looker Studio se mantendrá como plataforma gratuita y disponible para compartir dashboards con el público general.

### Cumplimiento y privacidad
El proyecto no recolecta información personal ni sensible de los usuarios. Se limita exclusivamente a datos públicos visibles en sitios web de ecommerce. Se respetarán los términos y condiciones de los sitios consultados, y se implementarán medidas para evitar una sobrecarga en sus servidores (ej. uso de sleep() o scraping espaciado).

### Accesibilidad
- El dashboard será accesible desde cualquier navegador moderno.
- Se priorizará el uso de tipografía clara, contraste alto y elementos responsivos para visualización en dispositivos móviles.
- Las visualizaciones incluirán etiquetas, tooltips y leyendas para facilitar su interpretación.

### Plan de despliegue

**Alcance inicial:**
- 3 ciudades (La Paz, Cochabamba, Santa Cruz)
- 3 supermercados por ciudad
- 20 productos seleccionados en categorías clave

**Prioridades:**
- Automatización del scraping
- Estructuración y limpieza de datos
- Desarrollo del dashboard público
- Generación de informes empresariales
- Diseño de dashboard privado o versión web ampliada

**Línea de tiempo estimada (Fase MVP):**
- Semana 1: configuración de entorno y scraping inicial
- Semana 2: estructura base de datos + almacenamiento
- Semana 3: Looker Studio con datos de prueba
- Semana 4: carga real y visualización pública

# 📊 Documento Estratégico

### Matriz de Aprobación (Sign-off Matrix)

| Nombre                     | Equipo / Rol           | Fecha        |
| -------------------------- | ---------------------- | ------------ |
| Rodrigo Jurgen Pinedo Nava | BI / Data Science Lead | \[Completar] |


**Proponente:** Rodrigo Jurgen Pinedo Nava

**Estado:** Draft > Under Review > ❏ Implemented | ☑ Not implemented

### 📁 Dataset principal
Datos scrapeados diariamente desde los sitios web de supermercados seleccionados (ecommerce públicos) en Bolivia.

### 📁 Dataset secundario
Información auxiliar sobre categorías, unidades de medida, marcas y estructura de productos.

### 👥 Perfiles de usuario

| Perfil               | Descripción y uso esperado del dashboard                                                               |
| -------------------- | ------------------------------------------------------------------------------------------------------ |
| Consumidores         | Consultan precios de productos específicos para decidir su compra diaria o semanal.                    |
| Empresas productoras | Analizan tendencias y comparaciones de precios para productos propios y de la competencia.             |
| Supermercados        | Evalúan su posicionamiento respecto al mercado local y regional.                                       |
| Periodistas / ONGs   | Utilizan los datos para estudios de inflación, informes de transparencia o investigaciones económicas. |

### 🧰 Funcionalidad del Dashboard

| Característica del Dashboard | Descripción solicitada                                             |
| ---------------------------- | ------------------------------------------------------------------ |
| Filtros dinámicos            | Ciudad, supermercado, categoría, subcategoría, marca, fecha        |
| Visualización interactiva    | Gráficos de líneas, barras y tablas dinámicas con filtros cruzados |
| Comparación de precios       | Entre marcas y supermercados por producto                          |
| Exportación de datos         | Opción de exportar tablas a CSV o PDF                              |
| Versión móvil optimizada     | Diseño responsivo y de carga ligera                                |
| Escalabilidad                | Adaptación futura a una app web con login para empresas            |

### 📌 Dashboard de referencia
No se utilizará un dashboard externo como referencia directa, pero se busca replicar el enfoque de simplicidad y claridad utilizado en herramientas como Precios Claros (Argentina) y dashboards de Google Trends.

### 🔐 Accesos

| Nivel de Acceso   | Detalle                                                       |
| ----------------- | ------------------------------------------------------------- |
| Público general   | Acceso completo al dashboard principal sin necesidad de login |
| Empresas (futuro) | Acceso privado a dashboards personalizados o informes         |
| Equipo técnico    | Acceso completo a datasets sin procesar y versiones de prueba |

### 📈 Alcance del dashboard
**Incluye:**
- Precios por producto y ciudad
- Categorías esenciales (alimentos, limpieza, higiene personal)
- Visualización de precios por unidad
- Evolución diaria de precios

**Excluye (por ahora):**
- Productos con variabilidad extrema o inconsistente (ej. frutas, verduras frescas)
- Tiendas sin catálogo online accesible
- Métodos de pago, promociones bancarias u ofertas limitadas

**🗓️ Filtros y granularidad temporal:**
- Filtro de fechas: sí, incluye selector de fechas desde/hasta.
- Granularidad: diaria (por defecto), con opción de agregación semanal o mensual.
- Rango inicial mostrado: últimos 7 días (por defecto).
- Comparación temporal: permite comparar contra periodo anterior (semana o mes anterior).

### 📊 Métricas y gráficos

**🎯 Objetivo visual: Ayudar a usuarios a responder rápidamente**
- ¿Cuál es el producto más barato hoy y dónde?
- ¿Cómo evoluciona el precio en el tiempo?
- ¿Cuál supermercado tiene los mejores precios promedio?
- ¿Cómo comparar marcas dentro de un mismo producto?

**🧱 Propuesta de estructura general del dashboard**

**🔹 Encabezado (header)**
- Título: Monitor de Precios Bolivia
- Fecha de actualización (última carga)
- Filtros generales: Ciudad, Categoría, Fecha desde/hasta

**🔸 Sección 1 – Tarjetas resumen por ciudad**

| Elemento visual            | Detalle                                                                                                                                                                                             |
| -------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 📍 **Tarjetas por ciudad** | Una tarjeta por ciudad (La Paz, Cochabamba, Santa Cruz) mostrando: <br> 🔹 Precio promedio de todos los productos <br> 🔹 Producto más barato del día <br> 🔹 Supermercado más económico en general |
| 🔀 **Interactividad**      | Al hacer clic en la tarjeta, filtra el resto del dashboard por esa ciudad                                                                                                                           |

**🔸 Sección 2 – Evolución de precios**

| Elemento visual         | Detalle                                                                  |
| ----------------------- | ------------------------------------------------------------------------ |
| 📈 **Gráfico de línea** | Evolución del precio de un producto seleccionado (ej. "Costilla de res") |
| Dimensiones             | Fecha en eje X, precio en Y, con líneas por supermercado o marca         |
| Filtros                 | Producto, ciudad, supermercado, marca                                    |

**🔸 Sección 3 – Comparativo de precios por categoría (Canasta Familiar)**

**🧺 Enfoque:** Comparar precios por categoría dentro de una canasta familiar predefinida
Ejemplo de categorías:

- Alimentos básicos (arroz, fideos, pan, azúcar)
- Proteínas (carne, pollo, huevo)
- Lácteos (leche, yogurt)
- Higiene (papel higiénico, jabón)
- Limpieza (lavandina, detergente)

**3.1 – Gráfico de barras apiladas por categoría**

| Detalle          | Valor                                                        |
| ---------------- | ------------------------------------------------------------ |
| Eje X            | Categoría de producto                                        |
| Eje Y            | Precio total (suma de productos seleccionados por categoría) |
| Segmento (color) | Supermercado o marca                                         |
| Uso              | Mostrar qué supermercado ofrece el mejor valor por categoría |

**3.2 – Tabla comparativa por categoría y supermercado**

| Categoría | Supermercado A | Supermercado B | Supermercado C |
| --------- | -------------- | -------------- | -------------- |
| Lácteos   | 23.50 Bs       | 21.90 Bs       | 25.30 Bs       |
| Proteínas | 88.70 Bs       | 91.20 Bs       | 85.00 Bs       |
| Higiene   | 15.40 Bs       | 14.80 Bs       | 16.50 Bs       |

- ✅ Se puede destacar en verde el menor precio por fila (categoría).
- ✅ Mostrar al pie el total general por supermercado (valor de la canasta completa).

**3.3 – Indicadores clave por canasta**

- Precio total de la canasta por supermercado
- Diferencia % entre el más caro y el más barato
- Producto más caro dentro de la canasta
- Supermercado más barato en X% de los productos

**🔸 Sección 4 – Tabla detallada con filtros**

| Elemento visual       | Detalle                                                                                          |
| --------------------- | ------------------------------------------------------------------------------------------------ |
| 📋 **Tabla dinámica** | Fecha – Ciudad – Supermercado – Producto – Precio – Unidad                                       |
| Extras                | ✅ Colores condicionales (verde = precio más bajo) <br> ✅ Filtros: marca, categoría, subcategoría |


**🔸 Sección 5 – Ranking o top productos**

| Elemento visual                                | Detalle                                                       |
| ---------------------------------------------- | ------------------------------------------------------------- |
| 🏆 **Top productos por diferencia de precios** | Ranking de productos con mayor dispersión entre supermercados |
| Ejemplo                                        | "Aceite de soya" → 10 Bs en tienda A y 17 Bs en tienda B      |


**🧩 Opcionales (futuro):**

- Elegir canastas personalizadas (familia pequeña, media, grande)
- Visualizar evolución del precio total de la canasta por semana
- Mostrar ahorro potencial si se combinan productos de distintos supermercados (opcional más adelante)

**🎨 Alternativa de navegación por producto**
También podés cambiar el enfoque:

Sección por producto → Costilla, Chorizo, Leche, Pan…

Cada uno con sus propias tarjetas resumen, visualización de evolución de precios, comparación entre supermercados y tabla detallada.

### 🎯 Beneficio para usuarios
- **Consumidores:** rápidamente detectan qué supermercado conviene según lo que más compran.
- **Productores:** entienden en qué categoría su producto compite en precio.
- **Supermercados:** visualizan si su oferta es competitiva por rubro, no solo por producto.

