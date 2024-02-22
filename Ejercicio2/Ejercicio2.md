# Ejercicio 2 - Portainer



**Utiliza una imagen de 'Portainer' para gestionar Docker.**

**Documenta la aplicación, su puesta en funcionamiento y realiza capturas de varias operaciones, por ejemplo:**



-Primero, descargamos la imagen de de Portainer Community Edition e iniciamos el contenedor de Portainer, en este caso, en el puerto 9000:

```bash
$ docker run -d -p 9000:9000 --name=portainer --restart=always -v /var/run/docker.sock:/var/run/docker.sock portainer/portainer-ce
```

![image-20240222173122958](./Ejercicio2.assets/image-20240222173122958.png)

-Luego, accedemos a `http://localhost:9000` y configuramos la contraseña de administrador:

![image-20240222173906779](./Ejercicio2.assets/image-20240222173906779.png)

-Y ya lo tendríamos listo para usar:

![image-20240222174541163](./Ejercicio2.assets/image-20240222174541163.png)

**- Capturas de algunas operaciones realizadas en Portainer:**

- **Muestra contenedores activos, para un contenedor, borra un contenedor.**

  -El dashboard:

  ![image-20240222174940645](./Ejercicio2.assets/image-20240222174940645.png)

  -Contenedores activos:

  ![image-20240222175304129](./Ejercicio2.assets/image-20240222175304129.png)

  -Paramos un contenedor:

  ![image-20240222175513541](./Ejercicio2.assets/image-20240222175513541.png)

  -Borramos un contenedor:

  ![image-20240222175614872](./Ejercicio2.assets/image-20240222175614872.png)

  ![image-20240222175712209](./Ejercicio2.assets/image-20240222175712209.png)

  ![image-20240222175826092](./Ejercicio2.assets/image-20240222175826092.png)

- **Muestra alguna operación con redes Docker.**

  -Las redes existentes:

  ![image-20240222180133244](./Ejercicio2.assets/image-20240222180133244.png)

  -Eliminamos una red:

  ![image-20240222180255085](./Ejercicio2.assets/image-20240222180255085.png)

  ![image-20240222180358051](./Ejercicio2.assets/image-20240222180358051.png)

- **Muestra alguna operación con volúmenes Docker.**

  -Los volúmenes actuales:
  
  ![image-20240222180642010](./Ejercicio2.assets/image-20240222180642010.png)
  
  -Este es uno de los volúmenes que tengo:
  
  ![image-20240222180813346](./Ejercicio2.assets/image-20240222180813346.png)
  
  -Eliminamos un volumen:
  
  ![image-20240222180844148](./Ejercicio2.assets/image-20240222180844148.png)

![image-20240222180929440](./Ejercicio2.assets/image-20240222180929440.png)
