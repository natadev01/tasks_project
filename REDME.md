
# Tasks Backend

Este es un proyecto sencillo de backend para gestionar tareas, construido con **Node.js**, **Express**, **pg** y **cors**. La base de datos utilizada es **PostgreSQL**, que se levantará en un contenedor Docker.

## Requisitos

- [Node.js](https://nodejs.org/) (v14 o superior)
- [Docker](https://www.docker.com/)
- npm

## Pasos para levantar el proyecto

### 1. Levantar la base de datos con Docker

Ejecuta el siguiente comando en la terminal para iniciar un contenedor de PostgreSQL:

```bash
docker run --name tasks-db -e POSTGRES_USER=user -e POSTGRES_PASSWORD=password -e POSTGRES_DB=tasks -p 5432:5432 -d postgres:latest
```

### 2. Crea la tabla `tasks` en PostgreSQL ejecutando el script SQL proporcionado

```sql
    CREATE TABLE tasks (

id SERIAL PRIMARY KEY,
title VARCHAR(255) NOT NULL,
completed BOOLEAN DEFAULT false
);

```

### 3. Instala las dependencias

```bash
   npm i
```

### 4. Ejecuta el servidor con

```bash
   npm start
```
