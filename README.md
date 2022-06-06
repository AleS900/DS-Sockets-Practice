# Práctica Sistemas Distribuidos

## Introducción
Los sockets son un mecanismo que nos permite establecer un enlace entre dos programas que se ejecutan independientes el uno del otro (generalmente un programa cliente y un programa servidor) Java por medio de la librería java.net nos provee dos clases: Socket para implementar la conexión desde el lado del cliente y ServerSocket que nos permitirá manipular la conexión desde el lado del servidor.

Los sockets han sido tradicionalmente la solución en torno a la cual se diseñan la mayoría de los sistemas de chat en tiempo real, proporcionando un canal de comunicación bidireccional entre un cliente y un servidor. 

Esto significa que el servidor puede enviar mensajes a los clientes. Cada vez que escribe un mensaje de chat, la idea es que el servidor lo obtenga y lo envíe a todos los demás clientes conectados.

## Explicación
A continuación se dará una breve explicación del código del presente trabajo:

### Clase Server
Esta clase es la responsable de escuchar las conexiones entrantes o clientes, además de crear un objeto socket para comunicarse con los mismos.

#### Consturctor: 
- Colocamos el constructor de la clase.

#### StartServer: 
Es el método encargado de mantener nuestro servidor corriendo
- El bucle es para que el programa siga corriendo mientrás el mismo no sea cerrado. (Utiliza el puerto 1234)
- Colocamos un TRY debido a que se necesita un manejo de los errores producto de los I/O.
- Se quiere que nuestro servidor este corriendo hasta que sea cerrado.
- Es un bloqueo, es decir que nuestro programa estará detenido hasta que un cliente se conecte, cuando esto sucede se retorna un objeto de tipo Socket el cual puede ser usado para comunicarse con el cliente.
- Cada objeto de esta clase será el responsable de la comunicación con un cliente, además implementa la  interfaz RUNNABLE la cual permite que las instancias de la misma sean ejecutadas en un hilo diferente. Esto es vital debido a que nosotros no podemos generar un nuevo hilo para manejar la conexión con cada nuevo cliente, esto haria que nuestra aplicación solamente pueda manejar un cliente a la vez.
- Creamos un objeto de tipo Thread para permitir la  ejecución simultanea de multiples peticiones.
- El método start inicia la ejecución de un hilo.
- Cuando se llama a start(), se llama al método de ejecución.
- El sistema operativo maneja los hilos.

#### CloseServerSocket
- Para cerrar el servidor.

#### Main
- Nuestro servidor esperará conexiones por parte de los clientes a este puerto 


#### Nota -Puerto 1234: 
El puerto TCP 1234 usa el Protocolo de Control de Transmisión. TCP es uno de los protocolos principales en redes TCP/IP. TCP es un protocolo orientado en la conexión, necesita el apretón de manos para determinar comunicaciones de principio a fin. Solo cuando la conexión es determinada, los datos del usuario pueden ser mandados de modo bidireccional por la conexión.

