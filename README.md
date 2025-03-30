Al momento de descargar o clonar el repositorio en tu local para que puedas ver las tablas de la base de datos debes copiar y pergar los siguientes comandos en la terminal de tu directorio actual

- docker cp backup.sql (El id o nombre de tu contenedor):/backup.sql   -> Este comando copia el backup en el contenedor
- docker exec -i 4d mysql -u root -p${MYSQL_ROOT_PASSWORD} ${MYSQL_DATABASE} < backup.sql  -> Este comando ejecuta el archivo backup para recuperar las tablas de la base de datos

Despues levanta tu contenedor y verifica que las tablas se hayan agregaso correctamente

