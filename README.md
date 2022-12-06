# **DOCKER**

### **Qué es un contenedor?**

es una manera de empaquetar aplicaciones con sus dependencias, incluyendo archivos de configuración.

- Portables (Fáciles de compartir)
- hace el despliegue y desarrollo más fácil
- se almacenan en un repositorio de contenedores (Docker Hub)

### **Qué es Docker Desktop?**

es una máquina virtual => Corre linux => Ejecuta contenedores

### **Comandos**

- **docker images**: devuelve las imagenes que se tengan descargadas
- **docker pull (paquete:(version=>opcional))**: descarga el paquete
- **docker image rm (paquete:(version))**: para eliminar imagenes
- **docker create (paquete)**: crea un contenedor con la imagen del paquete. Devuelve con resultado un id.
- **docker start (id)**: inicia un contenedor
- **docker ps**: devuelve los contenedores que están corriendo
- **docker stop (id)**: detiene un contenedor
- **docker ps -a**: muestra todos los contenedores
- **docker rm (nombre_contenedor)**: elimina un contenedor
- **docker create --name (nombre) (paquete)**: para crear un contenedor y definir el nombre
- **docker create -p27017:27017 --name monguito mongo**: crea un contenedor mapeando el puerto del host al puerto de
  docker(-pHOST:DOCKER)
- **docker logs (nombre_contenedor)**: se ven los logs del contenedor (--follow) continua escuchando los logs
- **docker run**: decarga la imagen si no existe, crea un contenedor y lo inicia, muestra los logs con la opcion --follow, para que no se muestren logs usar (-d) dettached  
- **docker create -p27017:27017 --name monguito -e MONGO_INITDB_ROOT_USERNAME=isra -e MONGO_INITDB_ROOT_PASSWORD=password mongo**: se deben buscar las variables de entorno necesarias para una imagen en docker 