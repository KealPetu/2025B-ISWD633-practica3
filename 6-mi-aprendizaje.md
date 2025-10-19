# COMPLETAR  
Comparando sus conocimientos antes de hacer la práctica con sus conocimientos después de hacer la tarea, explicar los principales aprendizajes logrados para beneficio de su formación profesional.  
Si solucionó un problema presentado o utilizó otros comandos que no se mencionan al realizar la práctica también se debe documentar.


Los aprendizajes principlaes de este taller que considero fueron muy interesantes fue la conexion de datos de los contenedores con el sistema del host, haciendo que cada vez que se crea una nueva instancia de un contenedor, este la informacion sea persistente y no sea elminada al momento que el contenedor deje de ejecutarse.

Es importante tener en cuenta la ubicacion donde montamos y creamos volumenes de nuestros contenedores, podemos especificar una ruta, como tambien podemos dejar que docker se encargue de ubicar los datos. Algunos volumenes pueden llegar a ser anonimos, lo que significa que son creados automaticamente y sirven como almacenamiento temporal, en tanto el contenedor exista.

Si existen volumentes anonimos, pero el contenedor con el que estaban ligados ya no existe, son llamados dangling volumenes.