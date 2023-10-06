# Tarea_5_JSP
---
## Sistema de Gestion de Empleados
###### Este es un proyecto de tarea para la universidad de un sistema de gestión de empleados en la web desarrollado en Java utilizando JSP y el entorno de desarrollo NetBeans. El objetivo de este proyecto es permitir a los usuarios gestionar información sobre empleados de una organización, incluyendo detalles como nombre, apellidos, dirección, teléfono, fecha de nacimiento y puesto. Ofrece funcionalidades básicas como agregar, modificar y eliminar registros de empleados. El proyecto fue desarrollado utilizando Apache NetBeans 18 como IDE
---
## Tecnologías Utilizadas

- Java
- JSP (Java Server Pages)
- HTML/CSS
- Bootstrap
- Base de datos (MySQL)
---

## Uso

###### 1. Clona este repositorio en tu máquina local.
###### 2. Asegúrate de tener Java JDK instalado.
###### 3. Abre el proyecto en Apache NetBeans 18 u otro entorno de desarrollo compatible.
###### 4. Configura una base de datos y asegúrate de actualizar la configuración de conexión en el código.
###### 5. Ejecuta la aplicación en tu servidor web.
---
## Base de Datos

###### La aplicación utiliza una base de datos para almacenar y recuperar la información de los empleados. Asegúrate de tener la base de datos configurada correctamente antes de ejecutar la aplicación.
```sql
CREATE DATABASE `db_empresa`;
USE `db_empresa`;

CREATE TABLE `empleados` (
  `id_empleado` int NOT NULL AUTO_INCREMENT,
  `codigo` varchar(20) DEFAULT NULL,
  `nombres` varchar(60) DEFAULT NULL,
  `apellidos` varchar(60) DEFAULT NULL,
  `direccion` varchar(100) DEFAULT NULL,
  `telefono` varchar(8) DEFAULT NULL,
  `fecha_nacimiento` date DEFAULT NULL,
  `id_puesto` smallint DEFAULT NULL,
  PRIMARY KEY (`id_empleado`),
  KEY `id_puesto_puesto_empreados_idx` (`id_puesto`),
  CONSTRAINT `id_puesto_puesto_empreados` FOREIGN KEY (`id_puesto`) REFERENCES `puestos` (`id_puesto`) ON UPDATE CASCADE
);

CREATE TABLE `puestos` (
  `id_puesto` smallint NOT NULL AUTO_INCREMENT,
  `puesto` varchar(40) DEFAULT NULL,
  PRIMARY KEY (`id_puesto`)
);
```
---
## Características

###### - Formulario para agregar, modificar y eliminar empleados.
######  - Visualización de la lista de empleados en una tabla ordenada.
###### - Captura de datos de empleados, incluyendo código, nombres, apellidos, dirección, teléfono y fecha de nacimiento.
###### - Selección de puestos a partir de un menú desplegable generado a partir de datos de la base de datos.
###### - Validación de entrada en el formulario.
###### - Uso de JavaServer Pages (JSP) para la programación en el lado del servidor.
###### - Interfaz de usuario sencilla y fácil de usar.
###### - Integración de Bootstrap para un diseño atractivo.
---
## Contribución

###### Contribuciones no son necesarias para esta tarea, ya que es un proyecto individual para la universidad.
---
