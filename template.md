# Especificación de requisitos 
## Del proyecto <project name>

Versión 0.1  
Generada por Sergio Morales Recio  
Clean-up  
13/04/2020  

Índice
=================
* [Versiones](#versiones)
* 1 [Introducción](#1-introducción)
  * 1.1 [Objetivo del documento](#11-objetivo-del-documento)
  * 1.2 [Ámbito del proyecto](#12-ámbito-del-proyecto)
  * 1.3 [Definiciones, acrónimos y abreviaturas](#13-definiciones-acrónimos-y-abreviaturas)
  * 1.4 [Referencias](#14-referencias)
  * 1.5 [Resumen del documento](#15-resumen-del-documento)
* 2 [Vista general del producto](#2-vista-general-del-producto)
  * 2.1 [Perspectiva del producto](#21-perspectiva-del-producto)
  * 2.2 [Funciones del producto](#22-funciones-del-producto)
  * 2.3 [Restricciones del producto](#23-restricciones-del-producto)
  * 2.4 [Perfiles de usuario](#24-perfiles-de-usuario)
  * 2.5 [Suposiciones y dependencias](#25-suposiciones-y-dependencias)
* 3 [Interfaces externas](#3-interfaces-externas)
    * 3.1 [Interfaces con el Usuario](#31-interfaces-con-el-usuario)
    * 3.2 [Interfaces con el Hardware](#32-interfaces-con-el-hardware)
    * 3.3 [Interfaces con el Software](#33-interfaces-con-el-software)
* 4 [Requisitos](#4-requisitos)
  * 4.1 [Precedencia y prioridad](#41-precedencia-y-prioridad) 
  * 4.2 [Funcionales](#42-funcionales)
  * 4.3 [Diseño e implementación](#43-diseño-e-implementación)
    * 4.3.1 [Instalación](#431-instalación)
    * 4.3.2 [Reusabilidad](#432-reusabilidad)
    * 4.3.3 [Fecha de Entrega](#433-fecha-de-entrega)
* 5 [Verificación](#5-verificación)
* 6 [Apendices](#6-apendices) 
  
## Versiones
| Name | Date    | Reason For Changes  | Version   |
| ---- | ------- | ------------------- | --------- |
|  Sergio Morales Recio    |   13/04/2020      |   Primera definición de requisitos   |       0.1    |
|      |         |                     |           |
|      |         |                     |           |

## 1. Introducción

### 1.1 Objetivo del documento
El propósito de este SRS es el describir cada una de las especificaciones del producto software a desarrollar por la organización Clean-up para informar a nuestro cliente.

### 1.2 Ámbito del proyecto
Nuestro software consiste en una plataforma en la que unos usuarios puedan subir incidencias o desperfectos en su ciudad en forma de tickets en los que prodrán incluir un titulo, una breve descripción, unas coordenadas y una o varias imágenes. Estos tickets son gestionados por unos agentes que se encargaran de solucionar los desperfectos y de cerrar los tickets. El objetivo de nuestro producto ofrecer un bien social al fomentar la comunicación entre los ciudadamos y el ayuntamiento de dicha ciudad al permitir que los ciudadanos aporten su grano de arena al mantenimiento de su cuidad.
### 1.3 Definiciones, acrónimos y abreviaturas

### 1.4 Referencias

### 1.5 Resumen del documento
En este documento veremos una descripción general del producto software, así como los requisitos del producto, sus interfaces y los metodos de verificación que se usarán en este.

## 2. Vista general del producto
![](https://github.com/Sermorrec/SRS-Template/blob/master/Diagrama%20casos%20de%20uso.PNG)
### 2.1 Perspectiva del producto
Algunas ciudades, como Málaga, poseen un sistema por el que los ciudadanos pueden poner reclamaciones o peticiones al ayuntamiento. Nos basamos en esta idea para generar un producto que realizase la misma función, enfocado en el matenimiento de la ciudad, de manera más rápida, sencilla y directa.

### 2.2 Funciones del producto
Nuestro producto consiste en un aplataforma web en la que los ciudadanos prodrán notificar al ayuntamiento de los distintos desperfectos que encuentren para que este lo solucione. Cada ciudadano deberá registrarse en el sistema creando una cuenta de usuario, una vez registrado podrá crear un ticket para nitificar de un desperfecto. Si las coordenadas de un ticket coinciden con las de otro ya creado el usuario podrá podrá decidir si son la misma y en tal caso también si subirla, en caso de subirla esta se añadira como un subticket del ticket principal o primero. Estos tickets seran tratados por los "agentes", que serian trabajadores del ayuntamiento, pudiendo comentarlos, modificar su estado y cerrarlos.

### 2.3 Restricciones del producto
Nuestra falta de experiencia nos impide desarrollar el producto como un aplicación móvil, lo que la haría muchos mas fácil y rápida de usar.

### 2.4 Perfiles de usuario
Los usuarios a los que está enfocado nuestro producto serían todos aquellos ciudadanos que esten dispuestos a ayudar de cierta manera a que su ciudad se mantenga en buen estado. 

### 2.5 Suposiciones y dependencias
Un factor que podría afectar a los requisitos establecidos serían los componentes software que usaríamos para desarrollar el producto. El caso más significativo sería el uso de Firebase de Google.
### 3 Interfaces externas

#### 3.1 Interfaces con el usuario 

#### 3.2 Interfaces con el Hardware

#### 3.3 Interfaces con el Software


## 4. Requisitos
A continucación se especificarán cada uno de los requisitos del producto a nivel del sistema siguiendo el siguiente formato
### ID - Nombre del requisito
Descripción
#### Dependencias 
#### Priodidad
#### Justificación

### 1 - Conexión a internet
Al tratarse de una plataforma web es necesario el tener una conexión a internet estable, así como un navegador que soporte HTML5
<br>Ninguna<br>
Fundamental
Es imprescindicle para el uso de sistema

### 2 - Cuenta única de usuario
Es necesario que cada uno de los usuarios se registre en el sistema aportando un nombre de usuario, un email, un número de telefono y una contraseña para hacer uso de él
<br>1
<br>Fundamental<br>
Para controlar la actividad de los usuarios y evitar el mal uso de la plataforma

### 3 - Verificación de cuenta por SMS
Una vez un usuario se registre en el sistema se verificará sus identidad mediante un SMS
<br>2 
<br>Fundamental<br>
Nos permite controlar que cada cuenta está asociada a una persona para evitar el uso de bots o la creación de varias cuentas por persona

### 4 - Inicio de sesión de usuarios
Para hacer uso del sistema es necesario que cada usuario inicie sesion una vez se hayan registrado
<br>1,3
<br>Fundamental<br>
Es imprescindible para el uso del sistema

### 5 - Creación de tickets
Cada usuario podrá notificar una incidencia en forma de ticket añadiendo un titulo, una breve descripción, coordenadas por medio de un GPS y/o imágenes
<br>1,4 
<br>Fundamental<br>
Es la función principal del sistema

### 6 - limitación tamaño de tickets
Se limita cada ticket a un maximo de 50mb en imágenes del formato JPG, PNG y el texto se limita a un máximo de 250 carácteres
<br>5
<br>Fundamental<br>
Reducir o limitar la carga en la base de datos

### 7 - Fusión de tickets
El sistema reconocerá si un ticket coincide en coordenadas con otro ya creado y preguntará al usuario si es el mismo, en el caso de que no lo sea se añadirá al sistema como un nuevo ticket, en caso de serlo se añadirá al ticket principal en forma de un subticket
<br>5
<br>Fundamental<br>
nos permite añadir mas información sobre una misma incidencia y aumentar el peso prioridad de esta

### 8 - Editar un ticket
El usuario tendrá la posibilidad de editar un ticket creado por él
<br>4
<br>Deseable<br>
Permite al usuario corregir errores que haya cometido al crear un ticket o simplemente modificar la información que haya aportado

### 9 - Términos y condiciones d uso
En la creación de una cuenta se le notificará al usuario los términos y condiciones de uso de la plataforma así como de toda la información legal
<br>2 
<br>Fundamental<br>
Nos permite establecer un uso correcto de la plataforma

### 10 - Página de inicio
Al iniciar sesion los usuarios dispondrán de un lista de incidencias cercanas en su página de inicio, mientras que los agentes dispondrán de un mapa en el que se les mostrará las incidencias
<br>4, 12
<br>Fundamental<br>
Es imprescindible para el uso del sistema

### 11 - Aplicación de escritorio
Los agentes, a diferencia de los usuarios, dispondrán de una aplicación de escritorio a la que accederám con una cuenta especial de agentes
<br>1,12
<br>Fundamental<br>
Facilita la gestión d elos tickets a los agentes

### 12 - Cuenta de agentes
Los agentes prodrán crear un cuenta especial mediante los administradores 
<br>1 
<br>Fundamental<br>
Permite al sistema diferenciar entre usuario y agente

### 13 - Inicio de sesión agentes
Para hacer uso del sistema los agentes deberán iniciar sesión mediante la aplicación de escritorio
<br>11, 12
<br>Fundamental<br>
Es imprescindible para que los agentes usen el sistema

### 14 - Modificar tickets
Los agentes podrán modificar los tickets, ya sea el estado de este, añadir comentarios o cerrarlos
<br>13
<br>Fundamental<br>
Permite a los agentes el gestionar los tickets

### 15 - Protección de datos
Para cumplir esta ley se usará un certificado SSL

<br>Fundamental<br>
Es necesaria para cumplir la ley

### 16 - Permisos
A la hora de crear una incidencia el sistema pedirá al usuario permisos para usar tanto el GPS, como la cámara, como el almacenamiento de archivos del dispositivo
<br>5
<br>Fundamental<br>
Es imprescindible para el uso del sistema

### 17 - Base de datos noSQL
Se usará una base de datos noSQL ya que es la mejor opción para nuestro sistema

<br>Fundamental<br>
Es imprescindible para el sistema


### 4.1 Precedencia y prioridad

| Id 	| Nombre 	| Descripción 	| Priodidad 	| Precedencia 	| Tipo 	|
|:--:	|:----------------------------:	|:----------------------------------------------------------------------------------------------------------------------------------------------------------------:	|:-------------------:	|:-----------:	|-----------	|
| 1	| Conexión a internet 	| Al tratarse de una plataforma web es necesario el tener una conexión a internet estable, así como un navegador que soporte HTML5 	| Fundamental 	|  	| Funcional 	|
| 2 | Cuenta única de usuario 	| Es necesario que cada uno de los usuarios se registre en el sistema aportando un nombre de usuario, un email, un número de telefono y una contraseña para hacer uso de él 	| Fundamental 	| 1 	| Funcional 	|
|  3	| Verificación de cuenta por SMS 	| Una vez un usuario se registre en el sistema se verificará sus identidad mediante un SMS 	| Fundamental 	| 2 	| No funcional 	|
|  4	| Inicio de sesión de usuarios 	| Para hacer uso del sistema es necesario que cada usuario inicie sesion una vez se hayan registrado 	| Fundamental 	| 1, 3 	| Funcional 	|
|  5	| Creación de tickets 	| Cada usuario podrá notificar una incidencia en forma de ticket añadiendo un titulo, una breve descripción, coordenadas por medio de un GPS y/o imágenes 	| Fundamental 	| 1, 4 	| Funcional 	|
|  6	| limitación tamaño de tickets 	| Se limita cada ticket a un maximo de 50mb en imágenes del formato JPG, PNG y el texto se limita a un máximo de 250 carácteres 	| Fundamental 	| 5 	| No funcional 	|
|  7	| Fusión de tickets 	| El sistema reconocerá si un ticket coincide en coordenadas con otro ya creado y preguntará al usuario si es el mismo, en el caso de que no lo sea se añadirá al sistema como un nuevo ticket, en caso de serlo se añadirá al ticket principal en forma de un subticket 	| Fundamental 	| 5 	| Funcional 	|
|  8	| Editar un ticket 	| El usuario tendrá la posibilidad de editar un ticket creado por él 	| Deseable 	| 4 	| Funcional 	|
|  9	| Términos y condiciones d uso 	| En la creación de una cuenta se le notificará al usuario los términos y condiciones de uso de la plataforma así como de toda la información legal 	| Fundamental 	| 2 	| Funcional	|
|  10	| Página de inicio 	| Al iniciar sesion los usuarios dispondrán de un lista de incidencias cercanas en su página de inicio, mientras que los agentes dispondrán de un mapa en el que se les mostrará las incidencias 	| Fundamental 	| 4, 12 	| No funcional 	|
|  	11  | Aplicación de escritorio 	| Los agentes, a diferencia de los usuarios, dispondrán de una aplicación de escritorio a la que accederám con una cuenta especial de agentes 	| Fundamental 	| 1, 12 	| Funcional   |
|  12	| Cuenta de agentes 	| Los agentes prodrán crear un cuenta especial mediante los administradores 	| Fundamental 	| 1 	|  Funcional	|
|  13	| Inicio de sesión agentes 	| Para hacer uso del sistema los agentes deberán iniciar sesión mediante la aplicación de escritorio 	| Fundamental 	| 11, 12 	| Funcional 	|
|  14	| Modificar tickets 	| Los agentes podrán modificar los tickets, ya sea el estado de este, añadir comentarios o cerrarlos 	| Fundamental 	| 13 	| Funcional 	|
|  15	| Protección de datos 	| Para cumplir esta ley se usará un certificado SSL 	| Fundamental 	|  	| Funcional 	|
|  16	| Permisos 	| A la hora de crear una incidencia el sistema pedirá al usuario permisos para usar tanto el GPS, como la cámara, como el almacenamiento de archivos del dispositivo 	| Fundamental 	| 5 	| Funcional 	|
|  17	|  Base de datos noSQL	| Se usará una base de datos noSQL ya que es la mejor opción para nuestro sistema 	| Fundamental 	|  	| No funcional 	|

	


### 4.2 Funcionales
[Documento casos de uso](https://github.com/Sermorrec/SRS-Template/blob/master/Casos%20de%20uso.pdf)

### 4.3 Diseño e implementación

#### 4.3.1 Instalación
Los usuarios deberan usar un navegador web complatible con HTML5 y los agentes deberán usar un sistema operativo W10 para poder instalar el cliente

#### 4.3.2 Reusabilidad
Usariamos Firebase de Google

#### 4.3.3 Fecha de entrega
5 de Junio de 2020

## 5. Verificación
Para verificar la aplicaion de escritorio se usará JUNIT y para el resto de requisitos se probará usando el sistema. 

## 6. Apendices
### Apéndice A: Ejemplos de este documento relleno
Incluir y referenciar en el documento tantos apéndices como sea necesario. Los siguientes, son ejemplo de este documento (con algunas modificaciones), relleno:

[Ejemplo relleno en inglés 1](https://arxiv.org/pdf/1005.0330.pdf)
[Ejemplo relleno en inglés 2](http://www.cse.chalmers.se/~feldt/courses/reqeng/examples/srs_example_2010_group2.pdf)

### Apéndice B: Generar PDF usando un fichero MD
Hay multitud de herramientas online y offline, por ejemplo: https://www.markdowntopdf.com/
