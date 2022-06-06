# Práctica Sistemas Distribuidos

## Introducción
Los sockets son un mecanismo que nos permite establecer un enlace entre dos programas que se ejecutan independientes el uno del otro (generalmente un programa cliente y un programa servidor) Java por medio de la librería java.net nos provee dos clases: Socket para implementar la conexión desde el lado del cliente y ServerSocket que nos permitirá manipular la conexión desde el lado del servidor.

</br>
 <p align="center">
    <img src="https://programacionextrema.com/wp-content/uploads/2015/10/sockets-java.jpg" />
 </p>

## Sistema de Chat en Tiempo Real - Sockets
Los sockets han sido tradicionalmente la solución en torno a la cual se diseñan la mayoría de los sistemas de chat en tiempo real, proporcionando un canal de comunicación bidireccional entre un cliente y un servidor. 

Esto significa que el servidor puede enviar mensajes a los clientes. Cada vez que escribe un mensaje de chat, la idea es que el servidor lo obtenga y lo envíe a todos los demás clientes conectados.

</br>
 <p align="center">
    <img src="https://media.geeksforgeeks.org/wp-content/uploads/20210902113314/ClientSocket.png" />
 </p>

## Explicación del Código
A continuación se dará una breve explicación del código del presente trabajo:

</br>
 <p align="center">
    <img src="https://i.ytimg.com/vi/-xKgxqG411c/maxresdefault.jpg" />
 </p>

### Clase Server
Esta clase es la responsable de escuchar las conexiones entrantes o clientes, además de crear un objeto socket para comunicarse con los mismos.
-  [Server Class](https://github.com/AleS900/DS-Sockets-Practice/blob/main/src/main/java/Server.java)

### Clase ClientHandler
Cuando un cliente se conecta, el servidor genera un hilo para manejar al cliente. De esta manera, el servidor puede manejar varios clientes al mismo tiempo.

Esta palabra clave debe usarse en setters, pasando el objeto como argumento, y llamar a constructores alternativos (un constructor con un conjunto diferente de argumentos).
-  [ClientHandler Class](https://github.com/AleS900/DS-Sockets-Practice/blob/main/src/main/java/ClientHandler.java)

### Clase Client
Es la responsable de escuchar las conexiones entrantes o clientes, además de crear un objeto socket para comunicarse con las mismas.
-  [Client Class](https://github.com/AleS900/DS-Sockets-Practice/blob/main/src/main/java/Client.java)
