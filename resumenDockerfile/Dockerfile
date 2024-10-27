# Paso 1: Define la imagen base
FROM debian:latest
# `FROM` define la imagen base de la cual partimos. Aquí elegimos Debian, pero puede variar según las necesidades.
# Otros ejemplos son `alpine`, `ubuntu`, o una imagen oficial de una aplicación específica.

# Paso 2: Instalar dependencias
RUN apt-get update && apt-get install -y nginx
# `RUN` ejecuta comandos dentro de la imagen. En este caso, actualiza los repositorios e instala Nginx.
# `&&` permite ejecutar múltiples comandos en una sola línea.
# Alpine --> RUN apk add <paquete>

# Paso 3: Copiar archivos al contenedor
COPY ./html /usr/share/nginx/html
# `COPY` copia archivos desde el host al contenedor. 
# El primer argumento (`./html`) es el directorio en el host, y el segundo (`/usr/share/nginx/html`) es el destino en el contenedor.
# Asegúrate de tener una carpeta `html` con archivos para que la copia funcione.

# Paso 4: Exponer un puerto
EXPOSE 80
# `EXPOSE` especifica el puerto en el que la aplicación escucha dentro del contenedor. Esto no abre el puerto en el host, pero indica que es el puerto de conexión esperado.

# Paso 5: Configurar el comando de inicio
CMD ["nginx", "-g", "daemon off;"]
# `CMD` define el comando predeterminado para ejecutar cuando el contenedor arranca.
# En este caso, ejecuta Nginx en primer plano (`daemon off`) para que el contenedor siga activo.
