# Proyecto_Fnial_Team_Champana

Integrantes:
- Nicolás Vargas Wilches. 
- Cesar Augusto Pérez González.
- Juan Esteban Pinilla

______________________________
1)
sintesis

(Oficina)
- montaje
Para el montaje en el area de oficinas, se utilizaron los siguientes elementos.
1) Servidor DHCP.
1) Pc de mesa, como administrador de la red.
1) MLSW (Multilayer Switch), tipo 3550-24Ps.
1) Router, tipo 2811.
1) WLC (Wireless LAN Controller)
1) AP (Access point), tipo 3702i
3) Laptop.
1) Smartphone.
1) Tablet.

Se hace la conexión que enlaza los elemntos. La mayoria son por cable de cobre directo a escepción de los dispositivos conectados por wireless.

- configuración
La configuración se realizó del siguiente modo. 

1. se configuraron las IPs fijas de cada elemento, acorde a la (Tabla 3. Tabla de direccionamiento red WLAN “Oficinas”) presentada en el proyecto.
- primero la del Servidor DHCP (requiere IP, la IP del DNS).
- luego la del WLC (requiere IP, mascara de subred, el gate way y la IP del DNS).
- el MLSW. (DHCP)

Luego se configuraron las IPs por DHCP de los demás dispositivos, como el PC, el AP, las laptops, la tablet y el celular.

Configuración del Router.
Se habilitan los puertos del rauter 0/0(enlace fuera del area oficina), 0/1.5 y 0/1.200 (enlace que conecta al MLSW con su respectiva direccioón IP [192.168.207.100  255.255.255.0]). Luego se configuran
Esta configuración del Router se puede evidenciar en la siguiente imagen.

![image](https://user-images.githubusercontent.com/110790300/199743508-baba5e1b-6efb-41e5-a0c3-03e6036ba56d.png)

Configuración del MLSW (Multilayer Switch)
Creamos la Vlan 5, 200 y luego habilitamos todos los puertos que conectal al MLSW. 
1/0/1 (enlace truncal al Router).
1/0/2 (enlace truncal al WLC).
1/0/3 (enlace truncal al AP).
1/0/4 (enlace de acceso Vlan200 al PC Administrador).
1/0/5 (enlace truncal al Servidor DHCP).
Esta configuración del MLSW se puede evidenciar en la siguiente imagen.

![image](https://user-images.githubusercontent.com/110790300/199749979-66592017-53a7-4e83-8859-3cee40734767.png)

Configuración IPs por DHCP
Utilizamos el servicio del servidor DHCP
requiere de la creación de un server pool, el gateway, el DNS, el inicio de IPs, mascara de subred(tipo c), numero max de usuarios y por ultimo la dirección del WLC.
con estos requerimientos los guardamos y prendemos el servicio. 
de esta forma automaticamente el PC Administrador y el AP, quedan asignados a una IP DHCP, de ingual forma se asigna una Dirección IP a los usuarios conectados por Wireless del AP.

Configuración del WLC desde el PC.
Al hacar la dirección DHCP, se hace un ping para verificar si estan conectados los dos.
luego pasamos a la busqeda web, ponemos la ip del WLC para ingresar y crear una cuenta de administrador como se muestra en la imagen.

![image](https://user-images.githubusercontent.com/110790300/199758325-ed2f7b15-8798-45fd-b68d-2b3b49d761bc.png)
![image](https://user-images.githubusercontent.com/110790300/199758517-81145435-5fd6-471b-a5ad-14b29fc97872.png)
![image](https://user-images.githubusercontent.com/110790300/199758664-7c1ce8fe-95b3-4c99-a7dd-350a375b6bdf.png)

Dentro del progrma crear el acceso de las Vlans con su respectiva seguridad para que el Wireless funcione.
Luego cada dispositivo lo conectamos por wireless como se muestra en la imagen.

![image](https://user-images.githubusercontent.com/110790300/199760328-7139e555-2980-4c69-a0f2-2d48ca682277.png)

Ahora los dispositivos estan listos para entrar a la pagina web.

(Mi Casa Inteligente)
-MONTAJE-
Para el montaje en la casa inteligente, se utilizaron los siguientes elementos:
1) Smartphone
1) PC de mesa genérico
1) Laptop
7) Dispositivos IoT (lámpara, ventilador, webcam, cafetera, puerta, ventana, puerta de garaje)
1) Home Gateway
1) Cable Modem PT
1) Cloud PT
1) Router 2811 (ISP)

Se hace la conexión que enlaza los elemntos. La mayoria son por wireless, a excepción del PC de mesa que se conecta por copper cable.

-CONFIGURACIÓN-
La configuración se realizó del siguiente modo. 

1. Se configura el Home Gateway con la IP que se nos provee para ello en la Tabla 2 del documento del Proyecto Final

![image](https://user-images.githubusercontent.com/98667419/199792538-ae20bdf7-728b-408b-92e5-3c124eee0e84.png)

2. Configuramos todos los dispositivos que deben de estar conectados al Home Gateway, esto teniendo en cuenta que su protocolo Gateway/DNS va a ser con DHCP.

Indicamos su SSID como HomeGateway

![image](https://user-images.githubusercontent.com/98667419/199793439-7bc9f798-6298-4aa7-a93d-2247ff475077.png)

Usamos protocolo DHCP

![image](https://user-images.githubusercontent.com/98667419/199793506-3ecff07a-8df0-4340-9674-d38e44e3642d.png)

También es necesario que se ubique el Home Gateway como IoT server para que los dispositivos vinculados a el puedan modificar las acciones que hacen cada uno de los aparatos.

3. Realizamos una configuración en el cableado del Cloud-PT

El Ethernet lo configuramos como Cable

![image](https://user-images.githubusercontent.com/98667419/199794881-4ea75cff-0942-4646-8fb0-74cdaedfb2c6.png)

Luego unimos el cable Coaxial7 al Ethernet6

![image](https://user-images.githubusercontent.com/98667419/199794942-0c99d432-096f-4d39-93b0-d661d98f2ef0.png)

4. En el router ISP, configuramos la IP respectiva, al igual que usamos unos comandos en el CLI para configurar el DHCP

IP Configurada

![image](https://user-images.githubusercontent.com/98667419/199795476-9be0c0cb-0d81-43cc-8450-8aa495b76a1e.png)

Comandos CLI en Router

![image](https://user-images.githubusercontent.com/98667419/199796485-16fec163-47a1-49f9-9ac6-94bf5bdb6868.png)

5)
Resultados
- configuración.
  
- verificación.
 Si entramos a la página web desde cualquier dispositivo de la casa inteligente que lo permita (PC de mesa, portátil o smartphone) podremos acceder sin problema a ella.
 
 ![image](https://user-images.githubusercontent.com/98667419/199802311-f92f66cf-6aad-4d64-9536-ed3ff4f17434.png)
 
 También podemos notar que podemos controlar las acciones de las IoT desde cualquier dispositivo conectado al Home Gateway a través del IoT Monitor, como se puede evidenciar a continuación.
 
 ![image](https://user-images.githubusercontent.com/98667419/199803841-4d17c87f-12e4-4242-a028-fcd63206cf63.png)

3)
Sección de Resultados y Análisis

4)
Concluciones, 

Recomendaciones:
Para la parte de oficinas se recomienda tener presente las direcciones DHCP como prioridad, para lograr la conectividad por wireless y lograr el ping con el WLC para crear la red WLAN.

Para la parte de Mi Casa Inteligente se recomienda tener muy en cuenta el protocolo DHCP que se tiene que configurar dentro del router, ya que esto es lo que permite que se pueda acceder adecuadamente a los servidores.

Para 
____________________________

Referencias.

https://youtu.be/AawECCXioFI

https://youtu.be/9R5vJt8zs90
