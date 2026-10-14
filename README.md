# 🛒 Java MySQL CRUD - Sistema de Gestión de Productos

[![Java](https://img.shields.io/badge/Java-ED8B00?style=for-the-badge&logo=openjdk&logoColor=white)](https://www.oracle.com/java/)
[![MySQL](https://img.shields.io/badge/MySQL-4479A1?style=for-the-badge&logo=mysql&logoColor=white)](https://www.mysql.com/)
[![JDBC](https://img.shields.io/badge/Driver-JDBC-007396?style=for-the-badge&logo=java&logoColor=white)](#)

Aplicación de consola desarrollada en **Java** que implementa las operaciones fundamentales de un **CRUD** (Crear, Leer, Actualizar, Eliminar) para la gestión de productos en una base de datos **MySQL**, aplicando el patrón de diseño **DAO (Data Access Object)**.

---

## 📌 Características Principales

- ➕ **Ingresar producto:** Registra nuevos elementos especificando nombre, precio y cantidad.
- 📋 **Mostrar productos:** Listado completo de los registros almacenados en la base de datos.
- 🔍 **Buscar producto:** Consulta rápida de productos por su ID o criterios específicos.
- ✏️ **Modificar producto:** Actualización dinámica de atributos de productos existentes.
- 🗑️ **Eliminar producto:** Remoción segura de registros por ID.
- 🏛️ **Arquitectura Limpia:** Separación de responsabilidades mediante patrón DAO y gestión centralizada de conexiones JDBC.

---

## 🛠️ Tecnologías e Integraciones

* **Lenguaje:** Java 8+
* **Base de Datos:** MySQL
* **Conector:** MySQL Connector/J (JDBC)
* **IDE Utilizado:** IntelliJ IDEA

---

## 🗄️ Estructura de la Base de Datos

Ejecuta el siguiente script SQL en tu gestor de base de datos MySQL para crear la base de datos y la tabla correspondiente:


CREATE DATABASE IF NOT EXISTS tienda;
USE tienda;

DROP TABLE IF EXISTS productos;

CREATE TABLE productos (
    id INT AUTO_INCREMENT PRIMARY KEY,
    nombre VARCHAR(100) NOT NULL,
    precio DECIMAL(10, 2) NOT NULL,
    cantidad INT NOT NULL
);


## 🚀 Instalación y Configuración Local

1. **Clonar el repositorio:**
```bash
git clone [https://github.com/ferzincal/java-mysql-crud.git](https://github.com/ferzincal/java-mysql-crud.git)
cd java-mysql-crud
```


2. **Configurar la Base de Datos:**
* Asegúrate de tener un servidor de MySQL corriendo (ej. MySQL Server, XAMPP o WAMP).
* Crea la base de datos utilizando el script SQL proporcionado arriba.


3. **Configurar Credenciales:**
* Abre la clase `DatabaseConnection.java` ubicada en `src/BDCRUD/` y actualiza la URL, usuario y contraseña de tu servidor MySQL local:
```java
String url = "jdbc:mysql://localhost:3306/tienda";
String user = "tu_usuario";
String password = "tu_password";
```

4. **Ejecutar la Aplicación:**
* Abre el proyecto en tu IDE preferido (IntelliJ IDEA, Eclipse o NetBeans).
* Agrega el driver `mysql-connector-j.jar` a las librerías/dependencias del proyecto si ejecutas manualmente.
* Ejecuta la clase `CRUD.java` para iniciar la interfaz de consola.


## 📝 Demostración del Menú de Consola

```text
***** Menú principal *****
1. Ingresar producto
2. Mostrar productos
3. Buscar producto
4. Modificar producto
5. Eliminar producto
6. Salir del menú principal

```

---

✨ *Desarrollado por [Daniel Sincal*](https://www.google.com/search?q=https://github.com/ferzincal)

```

```
