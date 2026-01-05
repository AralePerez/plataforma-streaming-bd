Proyecto Integrador – Bases de Datos Relacionales
Plataforma de Streaming Educativo

Integrantes

Pérez Flores Arale
Juarez Hipolito Marco Antonio


--Descripción del Dominio del Problema

Este proyecto modela una Plataforma de Streaming Educativo, cuyo objetivo es administrar cursos en línea, lecciones, usuarios, instructores y el progreso de aprendizaje de los estudiantes.

La base de datos permite:

Registrar usuarios e instructores.

Gestionar cursos y sus lecciones.

Controlar visualizaciones de contenido.

Asignar cursos a categorías.

Emitir certificados al completar cursos.

Realizar consultas complejas para análisis académico.

El proyecto fue desarrollado con el fin de aplicar conceptos fundamentales y avanzados de Bases de Datos Relacionales, tales como álgebra relacional, cálculo relacional y SQL.

--Esquema de la Base de Datos

La base de datos está compuesta por 8 tablas interconectadas, con más de 100 registros distribuidos de forma coherente:

Usuario

Instructor

Categoria

Curso

Leccion

Visualizacion

Curso_Categoria

Certificado

Todas las tablas cuentan con claves primarias y foráneas que garantizan la integridad referencial.

-- Diagrama Entidad–Relación Extendido (EER)

El diagrama EER del sistema se encuentra en el archivo de la practica 7,8,9


Este diagrama representa:

Entidades

Relaciones 1:N y N:M

Cardinalidades

Claves primarias y foráneas

--Modelo Relacional

El modelo relacional fue derivado a partir del diagrama EER y se encuentra documentado en el documento


Incluye:

Relaciones normalizadas

Atributos

Restricciones de integridad

--Instalación, Configuración y Ejecución de los Scripts
Requisitos

Docker Desktop

Navegador web

Git (opcional)

--Levantar el Entorno con Docker

Desde la carpeta raíz del proyecto, ejecutar:

docker-compose up -d


Esto iniciará los servicios de:

MySQL

phpMyAdmin

--Acceso a phpMyAdmin

Abrir el navegador y acceder a:

http://localhost:8080


Credenciales:

Servidor: mysql

Usuario: root

Contraseña: root

--Creación de la Base de Datos

En phpMyAdmin:

Seleccionar la pestaña SQL

Ejecutar el script:

sql/01_create_database.sql

--Creación de Tablas

Ejecutar el script:

sql/02_create_tables.sql


Este archivo crea todas las tablas y relaciones del sistema.

--Inserción de Datos

Ejecutar el script:

sql/03_insert_data.sql


Este script inserta más de 100 registros con datos realistas.

--Ejecución de Consultas

Las consultas pueden ejecutarse desde:

sql/04_queries.sql


Y se encuentran documentadas formalmente en:

/consultas/consultas_completas.md

--Consultas Implementadas

El proyecto incluye 20 consultas complejas, cada una expresada en:

Álgebra Relacional

Cálculo Relacional de Tuplas

Cálculo Relacional de Dominios

SQL

--Distribución:

5 consultas con operadores básicos

5 consultas con operadores de reunión

5 consultas con agrupación y agregación

3 consultas con operador de división

2 consultas con cuantificador universal (∀)

--Notas Técnicas

MySQL no soporta directamente operadores como división (÷) ni cuantificadores universales (∀).

Estos operadores fueron implementados mediante subconsultas con NOT EXISTS, respetando su equivalencia en álgebra relacional.

Todas las consultas fueron probadas en phpMyAdmin.

 --Conclusión

Este proyecto integra de forma completa el diseño, implementación y documentación de una base de datos relacional, demostrando la correcta aplicación de conceptos teóricos y prácticos requeridos en el curso
