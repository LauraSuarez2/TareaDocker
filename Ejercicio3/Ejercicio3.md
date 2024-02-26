# Ejercicio 3 - contenedores en red: Adminer y MariaDB



> Realizado por: Laura Suárez Suárez



1. **Crea una red bridge redbd**.

     ![image-20240223091817235](./Ejercicio3.assets/image-20240223091817235.png)

2. **Crea un contenedor con una imagen de mariaDB que estará en la red redbd . Este contenedor se ejecutará en segundo plano, y será accesible a través del puerto 3306. (Es necesario definir la contraseña del usuario root y un volumen de datos persistente)**.

     ```bash
     $ docker run -d --name mariadb-container -e MYSQL_ROOT_PASSWORD=1234 -p 3306:3306 --network redbd -v mariadb-data:/var/lib/mysql mariadb
     ```

     ![image-20240223093634125](./Ejercicio3.assets/image-20240223093634125.png)

3. **Crear un contenedor con Adminer que se pueda conectar al contenedor de la BD**.

     ```bash
     $ docker run -d --name adminer -p 8080:8080 --network redbd adminer
     ```

     ![image-20240223094352109](./Ejercicio3.assets/image-20240223094352109.png)

4. **Comprobar que el contenedor Adminer puede conectar con el contenedor mysql abriendo un navegador web y accediendo a la URL: http://localhost:8080. **

     ![image-20240223101302793](./Ejercicio3.assets/image-20240223101302793.png)

     ![image-20240223102438717](./Ejercicio3.assets/image-20240223102438717.png)

     **Entregar los siguientes Captura de pantalla y documentos y los comandos empleados para resolver cada apartado:**

  **-Captura de pantalla y documento donde se vean los contenedores creados y en ejecución**.

![image-20240223102554727](./Ejercicio3.assets/image-20240223102554727.png)

  **-Captura de pantalla y documento donde se vea el acceso a la BD a través de la interfaz web de Adminer.**

![image-20240223101302793](./Ejercicio3.assets/image-20240223101302793.png)

![image-20240223103012292](./Ejercicio3.assets/image-20240223103012292.png)

  **-Captura de pantalla y documento donde se vea la creación de una BD con la interfaz web Adminer.**

![image-20240223103231804](./Ejercicio3.assets/image-20240223103231804.png)

![image-20240223103249058](./Ejercicio3.assets/image-20240223103249058.png)

![image-20240223103458365](./Ejercicio3.assets/image-20240223103458365.png)

![image-20240223103533244](./Ejercicio3.assets/image-20240223103533244.png)

  **-Captura de pantalla y documento donde se entre a la consola del servidor web en modo texto y se compruebe que se ha creado la BD.**

![image-20240223104734371](./Ejercicio3.assets/image-20240223104734371.png)

![image-20240223104818988](./Ejercicio3.assets/image-20240223104818988.png)

![image-20240223104930552](./Ejercicio3.assets/image-20240223104930552.png)

**-Borrar los contenedores, la red y los volúmenes utilizados.**

Borramos los contenedores:

![image-20240226085005341](./Ejercicio3.assets/image-20240226085005341.png)

![image-20240226085046976](./Ejercicio3.assets/image-20240226085046976.png)

![image-20240226085302021](./Ejercicio3.assets/image-20240226085302021.png)

Borramos la red:

![image-20240226085201970](./Ejercicio3.assets/image-20240226085201970.png)

![image-20240226085317384](./Ejercicio3.assets/image-20240226085317384.png)

Y por último borramos el volumen:

![image-20240226085227655](./Ejercicio3.assets/image-20240226085227655.png)

![image-20240226085333836](./Ejercicio3.assets/image-20240226085333836.png)
