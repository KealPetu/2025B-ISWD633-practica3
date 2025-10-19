# BIND MOUNT
En un bind mount mapeamos (montar) un directorio o archivo específico del sistema de archivos del host con una parte del sistema de ficheros del contenedor.

```
docker run -d --name <nombre contenedor> -v <ruta carpeta host>:<ruta carpeta contenedor> <imagen> 
```
ó
```
docker run -d --name <nombre contenedor> --mount type=bind,source=<ruta carpeta host>,target=<ruta carpeta contenedor> <imagen>
```
- destination, dst, target: La ruta donde se monta el archivo o directorio en el contenedor.
- source, src: El origen del montaje.
  
### En tu computador crear una carpeta llamada nginx y dentro de esta carpeta crea otra llamada html. Como se aprecia en la figura.
![Volúmenes](directorio.PNG)

### Crear un contenedor con la imagen nginx:alpine, mapear todos por puertos, para la ruta carpeta host colocar el directorio en donde se encuentra la carpeta html en tu computador y para la ruta carpeta contenedor: /usr/share/nginx/html (esta ruta se obtiene al revisar la documentación de la imagen)
![Volúmenes](volumen-host.PNG)
# COMPLETAR CON EL COMANDO

### ¿Qué sucede al ingresar al servidor de nginx?
# COMPLETAR CON LA RESPUESTA A LA PREGUNTA

![resultado de ejecucion del contenedor](image.png)
Nos da como resultado un error, no existe un archivo html el que leer.

### ¿Qué pasa con el archivo index.html del contenedor?
# COMPLETAR CON LA RESPUESTA A LA PREGUNTA

![resultado](image-1.png)

No es creado, en los logs nos muestra que el contenedor no tiene indexado esta direccion.

### Ir a https://html5up.net/ y descargar un template gratuito, descomprirlo dentro de tu computador en la carpeta html
### ¿Qué sucede al ingresar al servidor de nginx?
# COMPLETAR CON LA RESPUESTA A LA PREGUNTA

![muestreo](image-4.png)

Ahora se muestra que el servidor esta utilizando el otro index.html.

### Eliminar el contenedor
# COMPLETAR CON EL COMANDO

![contenedor eliminado](image-3.png)

### ¿Qué sucede al crear nuevamente un contenedor montado al directorio definidos anteriormente?
# COMPLETAR CON LA RESPUESTA A LA PREGUNTA

![resultado](image-2.png)

Ahora el contenedor lee los archivos como si fueran suyos propios, en lugar de intentar crear uno nuevo.
