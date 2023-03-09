# iaw-practica-14-2
Practica 14-2


Voy a hacer una especie de introduccion de que va la practica. Estamos creandonos una instancia en la que en esa misma instancia vamos a usar docker para poder usar los contenedores y poder tener en una misma maquina instalado mysql, prestashop, phpmyadmin y el certificado.
Esto se dividira en redes y volumenes.

Para explicar practica vamos a dividirla en varios pasos:

**Paso 1:**
Vamos a crearnos una instancia con terraform, a esta maquina le vamos a añadir el grupo de seguridad y una ip elastica(esto esta explicado en las anteriores practicas). 

Muestro el grupo de seguridad:

![](../img/Fotos14-2/4.PNG)

Muestro la creacion de la instancia y de la ip elastica:

![](../img/Fotos14-2/5.PNG)

**Paso 2**
Hay que instalarnos docker y docker compose, para esto vamos a utilizar ansible:

![](../img/Fotos14-2/6.PNG)

Ahora vamos a añadir los paquetes de python para docker y movemos el directorio a la instancia:

![](../img/Fotos14-2/7.PNG)

**Paso 3**

Ahora tenemos que crearnos los contenedores, los volumenes y las redes en nuestra instancia.
Para esto vamos a usar la pagina docker hub para usar las imagines oficiales de las que vamos a usar.
En nuestro caso nos pide la practica usar las imagenes de phpmyadmin, prestashop, mysql y https-service.

Para prestashop:

![](../img/Fotos14-2/8.PNG)

Para mysql:

![](../img/Fotos14-2/9.PNG)

Para phpmyadmin:

![](../img/Fotos14-2/10.PNG)

Para https-portal(este seria el certificado como certbot):

![](../img/Fotos14-2/11.PNG)

Ahora muestro los volumenes y las redes:

![](../img/Fotos14-2/12.PNG)

Recordatorio= Para poder ejecutar docker compose hay que instalarse en nuestra maquina:

![](../img/Fotos14-2/1.PNG)

Las variables usadas son:

![](../img/Fotos14-2/13.PNG)

**Paso 4** 

Hay que asignar a nuestra ip un dominio, en mi caso he usado la pagina de noip.com:

![](../img/Fotos14-2/15.PNG)

Esto hay que añadirlo en nuestro https-portal.

**Paso 5**

Comprobamos que funciona, para esto vamos a poner nuestro dominio en nuestro navegador:

![](../img/Fotos14-2/2.PNG)

