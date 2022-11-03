# Proyecto_Fnial_Team_Champana

Integrantes:
- Nicolás Vargas Wilches. 
- Cesar Augusto Pérez González.
- Juan Esteban Pinilla

______________________________
1)
sintesia


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

Se hace la conección que enlaza los elemntos. la mayoria son por cable de cobre directo a escepción de los dispositivos conectados por wireless.

- configuración
La configuración se realizó del siguiente modo. 

1. se configuraron las IPs fijas de cada elemento, primero la del Servidor DHCP, luego la del WLC y el MLSW. Luego se configuraron las IPs por DHCP de los demás dispositivos, como el PC, el AP, las laptops, la tablet y el celular.

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



- verificación

2)
Resultados
- configuración.
- verificación.

3)
Sección de Resultados y Análisis

4)
Concluaionwa, recomendaciones.
____________________________

Referencias.
