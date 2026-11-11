# 📊 Employee Dashboard

[![Power BI](https://img.shields.io/badge/Power%20BI-F2C811?style=flat&logo=powerbi&logoColor=black)](https://powerbi.microsoft.com/)
[![DAX](https://img.shields.io/badge/DAX-0078D4?style=flat&logo=microsoft&logoColor=white)](https://learn.microsoft.com/en-us/dax/)
[![Power Query](https://img.shields.io/badge/Power%20Query-0078D4?style=flat&logo=microsoft&logoColor=white)](https://learn.microsoft.com/en-us/power-query/)
[![License](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)
[![Version](https://img.shields.io/badge/Version-1.0-blue.svg)]()

---

## 📋 Tabla de Contenidos

- [Descripción General](#-descripción-general)
- [Características Principales](#-características-principales)
- [Contenido del Proyecto](#-contenido-del-proyecto)
- [Herramientas y Tecnologías](#️-herramientas-y-tecnologías-utilizadas)
- [Configuración del Entorno](#️-configuración-del-entorno)
- [Estructura del Repositorio](#-estructura-del-repositorio)
- [Medidas DAX Implementadas](#-medidas-dax-implementadas)
- [Vistas Previas](#️-vistas-previas-del-proyecto)
- [Autor](#-autor)
- [Licencia](#-licencia)

---

## 📃 Descripción General

Dashboard de **Gestión de Empleados** desarrollado en Power BI, diseñado para analizar y visualizar información clave del personal de una organización de manera centralizada e interactiva. Este proyecto transforma datos de recursos humanos en información accionable mediante:

- 📊 **3 Vistas Analíticas:** Resumen General, Filtrado Female y Filtrado Male.
- 👥 **KPIs de Personal:** +4 medidas DAX esenciales (total de empleados, promedios de edad, evaluación y sueldo).
- 🎯 **Segmentación por Género:** Análisis diferenciado de métricas y distribución por masculino/femenino.
- 🖱️ **Navegación Interactiva:** Uso de marcadores (bookmarks) para un filtrado intuitivo y fluido entre páginas.
- 🎨 **Diseño Personalizado:** Lienzo con fondo SVG personalizado (Boxy sections) para una experiencia de usuario moderna.

---

## ✨ Características Principales

### 🔄 Transformaciones en Power Query
- Procesos de limpieza y modelado de datos para optimizar el rendimiento.
- Unificación de fuentes de datos CSV en un modelo relacional coherente.

### 📐 Modelo de Datos
- **Tablas Principales:** `Empleados`, `Evaluación` y `Sueldos`.
- Relaciones optimizadas entre las tablas para permitir un análisis multidimensional eficiente de los indicadores de recursos humanos.

### 🎨 Diseño Interactivo
- Navegación por páginas con paginado intuitivo mediante bookmarks.
- Segmentación de datos dinámica por género y otras características demográficas.
- Fondo de lienzo personalizado para una estética profesional y estructurada.

---

## 📊 Contenido del Proyecto

| Página | Descripción | Contenido Principal |
|--------|-------------|---------------------|
| **Resumen General** | Vista consolidada ejecutiva | KPIs globales, información relevante y métricas de todos los empleados de la organización. |
| **Filtrado Female** | Análisis por género femenino | Métricas, distribución y detalles específicos de las empleadas mujeres. |
| **Filtrado Male** | Análisis por género masculino | Métricas, distribución y detalles específicos de los empleados hombres. |

---

## 🛠️ Herramientas y Tecnologías Utilizadas

### Software Requerido
- **Power BI Desktop** (versión más reciente)

### Fuente de Datos
- 📄 Archivos CSV en la carpeta `Fuente de Datos/`:
  - `Empleados.csv`
  - `Evaluación.csv`
  - `Sueldos.csv`

### Lenguajes y Tecnologías
- **DAX** - Cálculo de medidas y KPIs de recursos humanos.
- **Power Query (Lenguaje M)** - Transformación, limpieza y estructuración de los datos CSV.

---

## ⚙️ Configuración del Entorno

### Prerequisitos
1. Descargar e instalar [Power BI Desktop](https://powerbi.microsoft.com/desktop/).

### Paso 1: Obtener el Proyecto
1. Clonar o descargar el repositorio completo.
2. Ubicar el archivo `Employee.pbix` (o `Employee.pbip` si se prefiere el formato de proyecto de Power BI).

### Paso 2: Cargar y Actualizar Datos
1. Abrir el archivo en Power BI Desktop.
2. Navegar a la pestaña **Inicio** en la cinta de opciones.
3. Hacer clic en el botón **Actualizar** (Refresh) para cargar los datos desde los archivos CSV configurados en la carpeta `Fuente de Datos`.
4. Si las rutas de los archivos cambian, ir a **Transformar datos** > **Configuración de origen de datos** y actualizar las rutas locales.

---

## 📂 Estructura del Repositorio

```text
.
├── Fuente de Datos/                  # Contiene los archivos de datos de ejemplo (.CSV)
│   ├── Empleados.csv
│   ├── Evaluación.csv
│   └── Sueldos.csv
├── Employee.Report/                  # Componentes del reporte (formato .pbip)
├── Employee.SemanticModel/           # Modelo semántico del proyecto
├── Dashboard (Boxy sections 6).svg   # Archivo de fondo personalizado para el lienzo del reporte
├── Employee.pbip                     # Proyecto Power BI (formato nuevo)
├── Employee.pbix                     # Archivo ejecutable de Power BI
├── Demo.gif                          # Demostración animada del funcionamiento del dashboard
├── .gitignore                        # Archivo de configuración Git
└── README.md                         # Este archivo de documentación
```

## 🧮 Medidas DAX Implementadas
El proyecto utiliza medidas DAX fundamentales para el análisis de recursos humanos, enfocadas en promedios y conteos distintos.

<details>
<summary>Ver medidas DAX del proyecto</summary>

#### 👥 Métricas de Personal

Total Empleados
Cuenta la cantidad única de empleados basándose en su identificador.

```dax
Total Empleados = DISTINCTCOUNT(Empleados[ID])
```

Promedio Edad
Calcula la edad promedio de los empleados en el contexto filtrado.

```dax
Promedio Edad = AVERAGE(Empleados[Edad])
```

Promedio Evaluación
Obtiene el promedio de las calificaciones de desempeño de los empleados.

```dax
Promedio Evaluación = AVERAGE(Evaluacion[Evaluación])
```

Promedio Sueldo
Calcula el salario promedio de los empleados en el contexto filtrado.

```dax
Promedio Sueldo = AVERAGE(Sueldos[Sueldo])
```

</details>

## 🖼️ Vistas Previas del Proyecto

<details>
<summary>📸 Ver Capturas de Pantalla</summary>

El repositorio incluye un archivo Demo.gif que muestra la interactividad, la navegación entre páginas y el filtrado dinámico del dashboard.
![Animation3](https://github.com/user-attachments/assets/dd68c611-92c6-4d13-88df-e5a39e78466e)

</details>

<details>
<summary>🎥 Ver Video Demostrativo</summary>

   
   Ver en YouTube: -
</details>

## 👤 Autor
Giancarlo Barrantes

Business Intelligence Developer | Power BI Specialist


<a href="https://www.linkedin.com/in/gb25"><img width="70" height="20" alt="image" src="https://github.com/user-attachments/assets/e0d69586-c6f9-4f66-9a3d-bc8dfa146463" /></a>
<a href="https://www.instagram.com/gbarrantes25"><img width="70" height="20" alt="image" src="https://github.com/user-attachments/assets/68773029-5e0f-49da-92e9-fb93a223dd09" />
</a>
<a href="https://www.tiktok.com/@gbarrantes25"><img width="65" height="20" alt="image" src="https://github.com/user-attachments/assets/349c87c0-1f3a-4368-8517-64a6012565c0" /></a>
<a href="https://www.youtube.com/@gbarrantes25"><img width="70" height="20" alt="image" src="https://github.com/user-attachments/assets/d9e2cb69-29ec-47fc-93ae-30896a7b533d" />
</a>

## 📝 Licencia
Este proyecto está bajo la Licencia MIT - ver el archivo <a href="https://mit-license.org/">LICENSE</a> para más detalles.

## ⭐ Agradecimientos
Si este proyecto te resultó útil, considera darle una ⭐ en GitHub y compartirlo con otros profesionales de Business Intelligence.

<div align="center">
   Hecho por <a href="https://gbarrantes25.github.io/">Giancarlo Barrantes</a>
</div>