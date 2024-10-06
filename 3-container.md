# Contenedores

### Crear un contenedor
Para crear un nuevo contenedor Docker a partir de una imagen específica, pero sin iniciarlo automáticamente. 

```
docker create --name <nombre contenedor> <nombre imagen>:<tag>
```
Crear el contenedor  **srv-web** usando la imagen nginx version alpine
![container_solu_01](img_solu/container_solu_01.png)

Si creas un contenedor en Docker sin asignarle un nombre específico utilizando la opción --name, Docker asignará automáticamente un nombre aleatorio al contenedor. Este nombre suele consistir en una combinación de palabras y números.  

Crear el contenedor usando la imagen hello-world
![container_solu_02](img_solu/container_solu_02.png)

### Listar los contenedores ejecutándose o no

```
docker ps -a
```

### Para iniciar un contenedor

```
docker start <nombre contenedor o identificador>
```
Iniciar el contenedor srv-web 
![container_solu_03](img_solu/container_solu_03.png)

### Listar los contenedores ejecutándose
```
docker ps 
docker ps | grep <nombre contenedor>
```

### Para detener un contenedor

```
docker stop <nombre contenedor>
```

### Para crear un contenedor y ejecutarlo inmediatamente

```
docker run --name <nombre contenedor> <nombre imagen>:<tag>
```
![Ecosistema de Docker](img/dockerRun.PNG)

Crear y ejecutar inmediatamente el contenedor **srv-web2** usando la imagen nginx:alpine
![container_solu_04](img_solu/container_solu_04.png)

## ¿Qué sucede luego de la ejecución del comando?
Se ejecuta inmediatamente y el terminal queda dentro de la ejecución del contenedor.
***

Cuando ejecutas un contenedor en primer plano sin la opción -d (modo detach), el contenedor captura la entrada estándar (stdin) del terminal, lo que significa que el terminal queda "atrapado" y no puedes introducir más comandos hasta que detengas el contenedor.

### Para crear un contenedor y ejecutarlo inmediatamente sin estar vinculados al mismo
-d: Es la opción que indica a Docker que ejecute el contenedor en segundo plano (en modo "detach").
Cuando un contenedor se ejecuta en segundo plano, Docker devuelve el control al terminal inmediatamente después de iniciar el contenedor, lo que permite al usuario seguir ejecutando otros comandos en el mismo terminal sin que el contenedor detenga la interacción.

```
docker run -d --name <nombre contenedor> <nombre imagen>:tag
```
Crear y ejecutar inmediatamente el contenedor **srv-web3** en modo detach usando la imagen nginx:alpine
![container_solu_05](img_solu/container_solu_05.png)

### Para eliminar un contenedor

```
docker rm <nombre contenedor>
```
Eliminar el contenedor que se creó a partir de la imagen hello-world 
![container_solu_06_a](img_solu/container_solu_06.png)

Verificar que el contenedor que se eliminó
![container_solu_06_b](img_solu/container_solu_06.png)

### Para eliminar un contenedor que esté ejecutándose

```
docker rm -f <nombre contenedor>
```
Eliminar el contenedor **srv-web3** 
![container_solu_07_a](img_solu/container_solu_07.png)

Verificar que el contenedor que se eliminó
![container_solu_07_b](img_solu/container_solu_07.png)

### Para inspecionar un contenedor 

Inspeccionar el contenedor **srv-web** 
![container_solu_08](img_solu/container_solu_08.png)
![container_solu_09](img_solu/container_solu_09.png)
![container_solu_10](img_solu/container_solu_10.png)
![container_solu_11](img_solu/container_solu_11.png)
![container_solu_12](img_solu/container_solu_12.png)
![container_solu_13](img_solu/container_solu_13.png)
![container_solu_14](img_solu/container_solu_14.png)
![container_solu_15](img_solu/container_solu_15.png)
![container_solu_16](img_solu/container_solu_16.png)
![container_solu_17](img_solu/container_solu_17.png)
![container_solu_18](img_solu/container_solu_18.png)
