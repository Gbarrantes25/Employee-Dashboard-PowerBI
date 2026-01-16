# Employee Dashboard

## 📃 Descripción General
El dashboard fue diseñado para un análisis básico del personal de la organización.


## 📊 Contenido del proyecto
- Página de resumen: Ofrece una vista consolidada de toda la infortación relevante de los empleados de la organización.
- Página Filtrado "Female": Contiene una vista de información sobre los empleados de género femenino.
- Página Filtrado "Male": Contiene una vista de información sobre los empleados de género masculino.


## 🛠️ Herramientas y Tecnologías Utilizadas
- Visualización: Power BI Desktop.
- Fuente de Datos:
  - [Empleados.csv](https://raw.githubusercontent.com/Gbarrantes25/Employee-Dashboard-PowerBI/refs/heads/main/Fuente%20de%20Datos/Empleados.csv)
  - [Evaluación.csv](https://raw.githubusercontent.com/Gbarrantes25/Employee-Dashboard-PowerBI/refs/heads/main/Fuente%20de%20Datos/Evaluacion.csv)
  - [Sueldos.csv](https://raw.githubusercontent.com/Gbarrantes25/Employee-Dashboard-PowerBI/refs/heads/main/Fuente%20de%20Datos/Sueldos.csv)
 
    
- Lenguajes: DAX para las medidas calculadas y Power Query (Lenguaje M) para la transformación de datos.


## ⚙️ Configuración del Entorno
- Software Necesario: Power BI Desktop.
- Instalación:
  - Descargar [Employee.pbix](https://github.com/Gbarrantes25/Employee-Dashboard-PowerBI/raw/refs/heads/main/Employee.pbix) con Power BI Desktop.
  - Entrar a Inicio y darle click a "Actualizar".


## 📂 Estructura del Repositorio
<code>.
  ├── Fuente de Datos/                  # Contiene los archivos de datos de ejemplo (.CSV)
  ├── Dashboard (Boxy sections 6).svg   # Es el archivo de fondo del lienzo del proyecto.
  ├── Employee.pbix                     # Archivo que será ejecutado con Power BI Desktop.
  └── README.md                         # Este archivo
</code>


## ✅ Características Principales
- Transformaciones en Power Query: Se realizaron procesos de limpieza y modelado de datos para optimizar el rendimiento.
- Medidas DAX: Se implementaron cálculos para análisis de empleados y segmentación por género.
  - <code>Promedio Edad = AVERAGE(Empleados[Edad])</code>
  - <code>Promedio Evaluación = AVERAGE(Evaluacion[Evaluación])</code>
  - <code>Promedio Sueldo = AVERAGE(Sueldos[Sueldo])</code>
  - <code>Total Empleados = DISTINCTCOUNT(Empleados[ID])</code>
- Diseño Interactivo: Uso de bookmarks para navegación y filtrado intuitivo entre páginas.


## 🖼️ Vistas Previas del proyecto
<details>
  <summary>Capturas</summary>

  ![Animation3](https://github.com/user-attachments/assets/dd68c611-92c6-4d13-88df-e5a39e78466e)


</details>


## 👤 Autor
- Giancarlo Barrantes
- Lima, Perú
- [Linkedin](https://www.linkedin.com/in/gb25/)
