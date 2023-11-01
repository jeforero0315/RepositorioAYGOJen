# RepositorioAYGOJen
1. Hacer la creación de la imagen de docker.
Primero se debe hacer la generación de la imagen docker del proyecto, se realiza de la siguiente manera:
![image](https://github.com/jeforero0315/RepositorioAYGOJen/assets/149447477/4e84f485-4007-4c80-95fe-4d961bd9218d)
2. Ir hacia Docker Desktop para visualizar la imagen que se creó
![image](https://github.com/jeforero0315/RepositorioAYGOJen/assets/149447477/7d9df86d-f131-4f5c-8bcc-653b0ec4dc23)
3. por medio del comando docker images, confirmamos la creación de la imagen, en este caso "dockersparkprimer"
![image](https://github.com/jeforero0315/RepositorioAYGOJen/assets/149447477/3be7b37f-bce7-4450-b941-1ee5a9d7b647)
4. Creación de una instancia para el contenedor de la imagen "dockersparkprimer"
-> Para este caso hacia el puerto físico 34000 al puerto 6000 de docker
![image](https://github.com/jeforero0315/RepositorioAYGOJen/assets/149447477/0cdae5b5-8acc-4733-a2ff-526ceedf2dab)
5. Ahora vamos a Docker Desktop para hacer la confirmación de que efectivamente se creó la instancia del contenedor:
![image](https://github.com/jeforero0315/RepositorioAYGOJen/assets/149447477/987aec2d-61dd-4243-8966-cf19765a7697)
6. como el contenedor se ejecuta de forma local, revisamos la siguiente direccion: http://localhost:34000/hello
![image](https://github.com/jeforero0315/RepositorioAYGOJen/assets/149447477/68ca40de-2731-4e57-8ec5-2278a65ff63f)
Teniendo en cuenta lo anterior, nos asegura de que la ejecucion de la instancia del contenedor se está ejecutandose correctamente.

--------------------------------------SEGUNDA PARTE ----------------AWS----------------------------------------
se debe subir la imagen a dockerHub y hacer el relacionamiento con los servicios de virtualizacion de AWS. 
Imagen del proyecto en dockerHub: https://hub.docker.com/r/jeforero0315/sparkprojectjeniffer
-> ![image](https://github.com/jeforero0315/RepositorioAYGOJen/assets/149447477/86a9e1bf-4a27-424e-aefd-a18c9a453d7f)
1. Teniendo en este punto el repositorio de dockerHub, se accede a AWS y se hace la creación de la maquina virtual junto con la llave de acceso
2. Se hizo la conexión hacia la maquina virtual y se instaló docker, teniendo lo anterior se creó una instancia del contenedor de la imagen subida al repositorio en dockerHub.
3. Máquina virtual creada apartir del servicio EC2 de AWS
![image](https://github.com/jeforero0315/RepositorioAYGOJen/assets/149447477/d562ec12-ea10-40d3-923d-46cb7eab1f9f)
4. Conexión a máquina virtual, se ejecuta el comando docker ps, el cual mostrará la instancia del contenedor en ejecución
![image](https://github.com/jeforero0315/RepositorioAYGOJen/assets/149447477/39e7f61d-e746-45a9-b40b-49e19fe0f8d2)
5. ejecución del comando sudo docker ps -a para ver las instancias creadas, se está ejecutando la instancia 0603b25703c4 por medio del puerto físico 42000 al puerto 6000 docker
![image](https://github.com/jeforero0315/RepositorioAYGOJen/assets/149447477/f04d59f7-eb72-4ff3-ae8a-8e85b3639c3b)
6. revisar por medio de la dirección
![image](https://github.com/jeforero0315/RepositorioAYGOJen/assets/149447477/034f9103-c88f-4363-b51c-56d5bb80adf9)
7. Ponemos en el navegaro la direccion DNS, agregamos el puerto en donde está escuchando que es 42000 y "/hello" lo cual está definido en el main del proyecto
![image](https://github.com/jeforero0315/RepositorioAYGOJen/assets/149447477/a63f3133-cce1-478a-a99b-fcb41a5ceb84)

