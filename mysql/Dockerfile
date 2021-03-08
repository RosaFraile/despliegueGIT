FROM mysql:5.7

ENV MYSQL_ROOT_PASSWORD root
ENV MYSQL_USER dwes
ENV MYSQL_PASSWORD dwes
ENV MYSQL_DATABASE dwes
COPY crearTablas.sql insertarDatos.sql /docker-entrypoint-initdb.d/
EXPOSE 3306
