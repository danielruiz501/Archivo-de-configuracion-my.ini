# Archivo de configuraciòn my.ini

1. Ubicación del archivo my.ini
- C:\ProgramData\MySQL\MySQL Server 8.0\my.ini
- C:\Program Files\MySQL\MySQL Server 8.0\my.ini
- C:\Windows\my.ini

2. Cómo abrirlo con permisos
- Abrir Bloc de notas como Administrador
- Archivo > Abrir > seleccionar my.ini

3. Parámetros más comunes para configurar
bind-address (permitir conexiones externas)
bind-address=0.0.0.0

Configurar el puerto
port=3306


Si se usa otro puerto, cámbiarlo:

port=3333

Tamaño de buffers (mejor rendimiento)
max_connections=200
innodb_buffer_pool_size=512M
query_cache_size=0


En MySQL 8.0 el query cache ya no existe, pero no causa error tenerlo en 0.

4. Guardar cambios y reiniciar MySQL

Muy importante: después de cambiar el archivo, reiniciar el servicio.

Desde servicios de Windows

Presiona Win + R

Escribir: services.msc

Busca MySQL80 o MySQL57

Clic derecho → Restart
