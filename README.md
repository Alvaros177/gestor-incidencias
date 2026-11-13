# Preguntas de la práctica Docker Compose

### 1. ¿Qué servicios forman la aplicación?

La aplicación está formada por tres servicios: frontend, backend y PostgreSQL.

### 2. ¿Por qué el backend está conectado a dos redes?

Porque necesita comunicarse con el frontend y con la base de datos. Para ello utiliza las redes `frontend` y `datos`.

### 3. ¿Qué servicio publica un puerto hacia el exterior?

El frontend publica el puerto 8080 para permitir acceder a la aplicación desde el navegador.

### 4. ¿Por qué no se publica el puerto de PostgreSQL?

Porque la base de datos solo necesita comunicarse con el backend mediante la red interna `datos`.

### 5. ¿Qué ventajas tiene utilizar Docker Compose?

Permite gestionar varios contenedores desde un único archivo y facilita iniciar, detener y administrar los servicios.

### 6. ¿Por qué se utilizan dos redes diferentes?

Para separar las comunicaciones entre los servicios y mejorar la organización y seguridad de la aplicación.

### 7. ¿Por qué el backend utiliza `db` para conectarse a PostgreSQL?

Porque Docker Compose permite utilizar el nombre del servicio como nombre de host dentro de la red.

### 8. ¿Qué diferencia hay entre detener un contenedor y eliminar los volúmenes?

Detener un contenedor no elimina los datos persistentes. Eliminar los volúmenes sí borra los datos almacenados en ellos.

### 9. ¿Qué ocurre si se pierde el volumen de PostgreSQL?

Se pierden los datos almacenados en la base de datos, por lo que sería necesario volver a introducirlos.
