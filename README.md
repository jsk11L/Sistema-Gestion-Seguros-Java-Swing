# Sistema de Gestión de Seguros (Java Swing)

![Java](https://img.shields.io/badge/Java-8%2B-007396?style=for-the-badge&logo=java)
![Apache Ant](https://img.shields.io/badge/Apache_Ant-A81C7D?style=for-the-badge&logo=apacheant)

Sistema de escritorio para la gestión de una compañía de seguros, desarrollado en **Java** con la biblioteca gráfica **Swing**.

Este proyecto fue desarrollado como parte del curso "Programación Avanzada" y demuestra una sólida aplicación del patrón de diseño **Modelo-Vista-Controlador (MVC)** y el manejo de archivos para la generación de reportes.

---

## 🖼️ Vistas de la Aplicación

*(Te recomiendo tomar capturas de pantalla de tu aplicación, subirlas al repositorio y poner los enlaces aquí. La `vistaMenu` sería ideal)*

`![Vista Principal](https/i.imgur.com/TU_FOTO_MENU.png)`
`![Vista Clientes](https/i.imgur.com/TU_FOTO_CLIENTES.png)`

---

## 🚀 Características Principales

El sistema permite la administración completa de los recursos de la empresa de seguros:

* **Gestión de Clientes:** Crear, modificar, eliminar y buscar clientes en el sistema.
* **Gestión de Planes:** Definir los diferentes planes de seguros que ofrece la compañía.
* **Gestión de Coberturas:** Administrar las coberturas asociadas a cada plan.
* **Exportación a Excel:** Genera un registro completo de la información en un archivo `.xls` (Excel) utilizando la biblioteca **JExcelApi (jxl)**.
* **Generación de Reportes:** Genera un reporte en formato `.csv` para análisis de datos.
* **Manejo de Excepciones:** Implementación de excepciones personalizadas para un manejo de errores robusto (ej. `ClienteNoEncontradoException`).

---

## 🏛️ Arquitectura del Software

El proyecto está construido siguiendo el patrón **Modelo-Vista-Controlador (MVC)**:

* **Modelo (`/src/modelos`)**: Contiene la lógica de negocio y las clases de datos (`Cliente`, `Plan`, `Cobertura`, `Empresa`).
* **Vista (`/src/vista`)**: Compuesta por todas las ventanas de la interfaz gráfica (`JFrame`) construidas con Java Swing.
* **Controlador (`/src/controladores`)**: Contiene la lógica que responde a los eventos de la vista (clicks, formularios) y actualiza el modelo (ej. `controladorCliente`, `controladorPlan`).

---

## 🛠️ Tecnologías Utilizadas

* **Java** (Lenguaje principal)
* **Java Swing** (Para la interfaz gráfica de escritorio)
* **JExcelApi (jxl)** (Biblioteca para la manipulación de archivos Excel `.xls`)
* **Apache Ant** (Para la automatización del build del proyecto)

---

## 🔧 Cómo Ejecutar el Proyecto

Este es un proyecto de **NetBeans** que utiliza **Apache Ant** para su compilación.

### Opción 1: Usando un IDE

1.  Abre NetBeans (o un IDE compatible como IntelliJ IDEA).
2.  Selecciona `Archivo > Abrir Proyecto`.
3.  Navega a la carpeta raíz de este repositorio y ábrela.
4.  Ejecuta el proyecto (normalmente con `F6` o el botón "Play"). El IDE detectará automáticamente el `build.xml`.

### Opción 2: Usando la línea de comandos (con Ant)

Si tienes Apache Ant instalado en tu sistema:

1.  **Clona el repositorio:**
    ```bash
    git clone [https://github.com/tu-usuario/Sistema-Gestion-Seguros-Java-Swing.git](https://github.com/tu-usuario/Sistema-Gestion-Seguros-Java-Swing.git)
    cd Sistema-Gestion-Seguros-Java-Swing
    ```

2.  **Compila el proyecto (crea el .jar):**
    ```bash
    ant jar
    ```

3.  **Ejecuta el archivo `.jar` compilado:**
    *(El nombre del .jar puede variar según la configuración de `build.xml`, pero usualmente será algo así)*
    ```bash
    java -jar dist/PA-Proyecto-G8.jar
    ```
