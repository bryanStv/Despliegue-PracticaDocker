# Usamos la imagen base oficial de Debian
FROM debian:latest

# Configuramos la zona horaria y el idioma
ENV TZ=Europe/Madrid
ENV LANG=C.UTF-8

# Actualizamos el sistema y añadimos paquetes necesarios
RUN apt-get update && apt-get upgrade -y && \
    apt-get install -y curl nano

# Definir el comando de inicio predeterminado
CMD ["/bin/bash"]