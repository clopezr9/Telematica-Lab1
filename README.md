# Telematica-Lab1
## Autor: Catalina López Roldán

## Descripción
En este laboratorio se puede evidenciar el manejo de sockets y de arquitectura cliente/servidor por medio de un chat grupal, donde dos clientes o mas se van a poder comunicar siempre y cuando el servidor este corriendo. 

## Instalación
Se debe instanciar tres o mas instancias EC2 en AWS, una de esta sera el servidor y las otras los clientes que se van a comunicar en el chat grupal. 
Estas instancias deben tener dos grupos de seguridad (SG) diferentes, el SG del Servidor debe tener el puerto seleccionado para TCP, en este caso se seleccionó el 3550, abierto para cualquir IP. Por otro lado el puesto TCP del SG de los clientes, que va con el mismo numero, debe estar solo abierto para la IP publica del Servidor. Hay que tener en cuenta que la instancia del Servidor debe llevar una IP elastica asociada.

Todas las instancias deben contra con python 3, ademas de git y un edito de texto de preferencia, se pueden instalar con los siguientes comandos:
<pre><code> $ sudo yum install git
 $ sudo yum install emacs 
 $ sudo yum install python3
</code></pre>

## Ejecución
Para ejecutar el programa se debe acceder a las instancias por medio de ssh y clonar el repositorio. Posteriormente se debe modificar la IP que en los archivos Client1.py para asegurarse de que coincida con la instancia del servidor creado. Por otro lado en el el archivo de Client1.py y Server.py los puertos deben ser los mismo.
Luego de verificar esto se debe correr en la instancia servidor el archivo Server.py de la siguiente manera:
<pre><code> $ python3 Server.py
</code></pre>
Luego de tener el servidor corriendo se puede poner a correr los clientes que se desee de la siente manera:
<pre><code> $ python3 Client1.py
</code></pre>
Al correr este comnado se mostrara en el servidor la IP de cada uno de los clientes que estan conectados.
