## Web Scraping

## Requisitos de los interesados

- **Proyecto:** Sistema de Monitoreo de Precios en Supermercados de Bolivia
- **BI Professional:** Rodrigo Jurgen Pinedo Nava
- **Client/Sponsor:** Proyecto personal con posibilidades de escalar hacia alianzas institucionales o comerciales

**Problema de negocio**

En el actual contexto de crisis económica e inflación persistente en Bolivia, los consumidores enfrentan dificultades para identificar los precios más convenientes de productos esenciales en supermercados. Al mismo tiempo, las empresas productoras y los supermercados carecen de herramientas públicas que les permitan visualizar en tiempo real la evolución del mercado y los precios de la competencia. Este proyecto se propone abordar ambas problemáticas mediante la automatización del relevamiento de precios en línea y su posterior visualización dinámica.

**Stakeholders principales**

- **Ciudadanía consumidora:** interesada en acceder a precios actualizados para optimizar sus decisiones de compra.
- **Empresas productoras y distribuidoras:** buscan monitorear la presencia y precios de sus productos en distintos supermercados.
- **Supermercados:** interesados en analizar su posicionamiento frente a la competencia y ajustar sus estrategias de precios.
- **Periodistas de datos y organizaciones no gubernamentales:** potenciales usuarios del conjunto de datos para análisis socioeconómicos.

**Uso previsto por stakeholders**

- **Consumidores:** acceden a gráficos o tablas que les permiten comparar precios y marcas de forma sencilla.
- **Productores/competidores:** utilizan dashboards privados o informes descargables con datos históricos y análisis comparativos.
- **Supermercados:** reciben reportes personalizados que muestran su evolución de precios y posicionamiento relativo.
- **Periodistas/analistas:** descargan datasets estructurados para estudios externos y reportes públicos.

**Requerimientos principales**

- Implementación de un sistema automatizado de scraping diario de precios a partir de sitios de ecommerce de supermercados seleccionados.
- Almacenamiento estructurado de los datos recolectados, incluyendo los siguientes metadatos: fecha, ciudad, supermercado, sucursal, marca, categoría, subcategoría, nombre del producto, identificador único del producto, precio y unidad.
- Desarrollo de un dashboard público, inicialmente con Looker Studio, orientado a la ciudadanía en general.
- Generación de informes comparativos descargables, organizados por producto y supermercado.
- Escalabilidad del sistema hacia una aplicación web o móvil en fases futuras del proyecto.
- Potencial monetización del servicio mediante accesos premium o suscripciones destinadas a empresas del rubro.

## Requisitos del proyecto

**Propósito - Impacto social**

El proyecto busca brindar a la ciudadanía boliviana una herramienta accesible para conocer los precios actualizados de productos esenciales en supermercados de las ciudades de La Paz, Cochabamba y Santa Cruz. En paralelo, se construirá una base de datos histórica que permitirá generar visualizaciones interactivas para distintos perfiles de usuarios, incluyendo consumidores, empresas productoras y cadenas de supermercados. Dada la coyuntura económica nacional, el proyecto se posiciona como una solución de transparencia de precios y monitoreo del mercado minorista.

**Dependencias clave**
- **Equipo de desarrollo:** conformado actualmente por el analista BI responsable del proyecto, encargado del scraping, modelado de datos, y desarrollo del dashboard.
- **Fuentes de datos:** sitios web de ecommerce de supermercados seleccionados (ej. Hipermaxi, Fidalga, IC Norte, Amarket, otros).
- **Herramientas:** Python para scraping automatizado, Google Sheets para almacenamiento inicial, Looker Studio para visualización.
- **Entregables esperados:**
  - Scripts de scraping funcionales y automatizados.
  - Base de datos estructurada de precios históricos.
  - Dashboard público con visualizaciones clave por producto, ciudad y supermercado.
  - Informes descargables para empresas interesadas.

**Requisitos de los stakeholders**

Basados en el Documento de Requisitos de los Interesados, los requerimientos han sido priorizados de la siguiente forma:

|Requisito|	Prioridad|
|---------|----------|
|Automatización diaria del scraping de precios|	R|
|Almacenamiento estructurado de datos históricos|	R|
|Dashboard público con filtros por ciudad, categoría y producto|	R|
|Visualización de series temporales y comparaciones entre supermercados|	R|
|Posibilidad de exportar informes en formatos abiertos (CSV/PDF)|	D|
|Dashboard privado para empresas productoras o supermercados|	D|
|Acceso restringido para perfiles empresariales mediante login o token|	N|
|Integración futura con apps móviles|	N|

**Nota:** R - requerido, D - deseado, N - agradable tener

**Criterios de éxito**

Se considerará exitoso este proyecto si se cumplen los siguientes indicadores SMART:
- Automatización diaria del scraping de al menos 3 supermercados por ciudad sin errores durante 30 días consecutivos.
- Almacenamiento correcto de más de 1.000 registros únicos de productos en un lapso de un mes.
- Publicación del dashboard funcional en Looker Studio con al menos tres visualizaciones interactivas: evolución de precios, comparativo por ciudad y ranking de supermercados.
- Acceso público al dashboard validado por al menos 100 usuarios únicos en su primer mes de lanzamiento.

**Recorrido del usuario (User journeys)**

**Experiencia actual:**
Los consumidores deben visitar múltiples sitios web manualmente para buscar precios, sin garantías de actualización ni posibilidad de comparar entre supermercados o ciudades. Las empresas productoras no cuentan con herramientas para auditar precios públicos de sus productos ni analizar el mercado minorista con datos abiertos.

**Experiencia futura ideal:**
Los usuarios acceden a una plataforma que centraliza la información de precios, les permite comparar, visualizar tendencias y descargar información útil. Las empresas pueden explorar reportes históricos y tomar decisiones informadas sobre pricing y posicionamiento.

**Supuestos**

- Las páginas de ecommerce de supermercados seguirán siendo accesibles públicamente sin necesidad de autenticación.
- Los productos mantienen estructuras HTML reconocibles para los scrapers durante la duración del proyecto.
- Looker Studio se mantendrá como plataforma gratuita y disponible para compartir dashboards con el público general.

**Cumplimiento y privacidad**

El proyecto no recolecta información personal ni sensible de los usuarios. Se limita exclusivamente a datos públicos visibles en sitios web de ecommerce. Se respetarán los términos y condiciones de los sitios consultados, y se implementarán medidas para evitar una sobrecarga en sus servidores (ej. uso de sleep() o scraping espaciado).

**Accesibilidad**

- El dashboard será accesible desde cualquier navegador moderno.
- Se priorizará el uso de tipografía clara, contraste alto y elementos responsivos para visualización en dispositivos móviles.
- Las visualizaciones incluirán etiquetas, tooltips y leyendas para facilitar su interpretación.

**Plan de despliegue**

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

## Documento estratégico

| Nombre                     | Equipo / Rol           | Fecha        |
| -------------------------- | ---------------------- | ------------ |
| Rodrigo Jurgen Pinedo Nava | BI / Data Science Lead | \[Completar] |

**Proponente:** Rodrigo Jurgen Pinedo Nava

**Estado:** Borrador > En revisión > ❏ Implementado | ☑ No implementado

📁 **Dataset principal**

Datos scrapeados diariamente desde los sitios web de supermercados seleccionados (ecommerce públicos) en Bolivia.

📁 **Dataset secundario**

Información auxiliar sobre categorías, unidades de medida, marcas y estructura de productos.

**Perfiles de usuario**

| Perfil               | Descripción y uso esperado del dashboard                                                               |
| -------------------- | ------------------------------------------------------------------------------------------------------ |
| Consumidores         | Consultan precios de productos específicos para decidir su compra diaria o semanal.                    |
| Empresas productoras | Analizan tendencias y comparaciones de precios para productos propios y de la competencia.             |
| Supermercados        | Evalúan su posicionamiento respecto al mercado local y regional.                                       |
| Periodistas / ONGs   | Utilizan los datos para estudios de inflación, informes de transparencia o investigaciones económicas. |

**Funcionalidad del Dashboard**

| Característica del Dashboard | Descripción solicitada                                             |
| ---------------------------- | ------------------------------------------------------------------ |
| Filtros dinámicos            | Ciudad, supermercado, categoría, subcategoría, marca, fecha        |
| Visualización interactiva    | Gráficos de líneas, barras y tablas dinámicas con filtros cruzados |
| Comparación de precios       | Entre marcas y supermercados por producto                          |
| Exportación de datos         | Opción de exportar tablas a CSV o PDF                              |
| Versión móvil optimizada     | Diseño responsivo y de carga ligera                                |
| Escalabilidad                | Adaptación futura a una app web con login para empresas            |

**Dashboard de referencia**

No se utilizará un dashboard externo como referencia directa, pero se busca replicar el enfoque de simplicidad y claridad utilizado en herramientas como Precios Claros (Argentina) y dashboards de Google Trends.

**Accesos**

| Nivel de Acceso   | Detalle                                                       |
| ----------------- | ------------------------------------------------------------- |
| Público general   | Acceso completo al dashboard principal sin necesidad de login |
| Empresas (futuro) | Acceso privado a dashboards personalizados o informes         |
| Equipo técnico    | Acceso completo a datasets sin procesar y versiones de prueba |

**Alcance del dashboard**
**Incluye:**
- Precios por producto y ciudad
- Categorías esenciales (alimentos, limpieza, higiene personal)
- Visualización de precios por unidad
- Evolución diaria de precios

**Excluye (por ahora):**
- Productos con variabilidad extrema o inconsistente (ej. frutas, verduras frescas)
- Tiendas sin catálogo online accesible
- Métodos de pago, promociones bancarias u ofertas limitadas

**Filtros y granularidad temporal**
- **Filtro de fechas:** sí, incluye selector de fechas desde/hasta.
- **Granularidad:** diaria (por defecto), con opción de agregación semanal o mensual.
- **Rango inicial mostrado:** últimos 7 días (por defecto).
- **Comparación temporal:** permite comparar contra periodo anterior (semana o mes anterior).

**Métricas y gráficos**

🟦 **Gráfico 1**
| Característica     | Detalle                           |
| ------------------ | --------------------------------- |
| Título del gráfico | Evolución del precio por producto |
| Tipo de gráfico    | Línea                             |
| Dimensiones        | Fecha, marca, supermercado        |
| Métricas           | Precio promedio, precio mínimo    |

🟨 **Gráfico 2**
| Característica     | Detalle                                   |
| ------------------ | ----------------------------------------- |
| Título del gráfico | Comparación de precios por ciudad         |
| Tipo de gráfico    | Barras agrupadas                          |
| Dimensiones        | Ciudad, supermercado                      |
| Métricas           | Precio promedio por producto seleccionado |

🟩 **Gráfico 3**
| Característica     | Detalle                                   |
| ------------------ | ----------------------------------------- |
| Título del gráfico | Tabla dinámica de precios detallados      |
| Tipo de gráfico    | Tabla con filtros y colores condicionales |
| Dimensiones        | Fecha, ciudad, supermercado, producto     |
| Métricas           | Precio, unidad, variación diaria          |

🧪 **Maqueta del dashboard (mockup)**

[Se incluirá más adelante un boceto visual en Figma o imagen capturada del prototipo en Looker Studio]
