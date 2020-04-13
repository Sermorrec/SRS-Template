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
  * 4.3 [Calidad de Servicio](#43-calidad-de-servicio)
    * 4.3.1 [Rendimiento](#431-rendimiento)
    * 4.3.2 [Seguridad](#432-seguridad)
    * 4.3.3 [Fiabilidad](#433-fiabilidad)
    * 4.3.4 [Disponibilidad](#434-disponibilidad)
  * 4.4 [Normativas aplicables](#44-normativas-aplicables)
  * 4.5 [Diseño e implementación](#45-diseño-e-implementación)
    * 4.5.1 [Instalación](#451-instalación)
    * 4.5.2 [Distribución](#452-distribución)
    * 4.5.3 [Mantenimiento](#453-mantenimiento)
    * 4.5.4 [Reusabilidad](#454-reusabilidad)
    * 4.5.5 [Portabilidad](#455-portabilidad)
    * 4.5.6 [Coste](#456-coste)
    * 4.5.7 [Fecha de Entrega](#457-fecha-de-entrega)
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

### 2.1 Perspectiva del producto
Algunas ciudades, como Málaga, poseen un sistema por el que los ciudadanos pueden poner reclamaciones o peticiones al ayuntamiento. Nos basamos en esta idea para generar un producto que realizase la misma función, enfocado en el matenimiento de la ciudad, de manera más rápida, sencilla y directa.
### 2.2 Funciones del producto
Nuestro producto consiste en un aplataforma web en la que los ciudadanos prodrán notificar al ayuntamiento de los distintos desperfectos que encuentren para que este lo solucione. Cada ciudadano deberá registrarse en el sistema creando una cuenta de usuario, una vez registrado podrá crear un ticket para nitificar de un desperfecto. Si las coordenadas de un ticket coinciden con las de otro ya creado el usuario podrá podrá decidir si son la misma y en tal caso también si subirla, en caso de subirla esta se añadira como un subticket del ticket principal o primero. Estos tickets seran tratados por los "agentes", que serian trabajadores del ayuntamiento, pudiendo comentarlos, modificar su estado y cerrarlos.
[!Casos](Diagrama casos de uso.PNG)
### 2.3 Restricciones del producto
Esta subsección debe proporcionar una descripción general de cualquier otro elemento que limitará las opciones del desarrollador. Estos pueden incluir:

* Interfaces para usuarios, otras aplicaciones a usar o limitaciones hardware.
* Restricciones de calidad de servicio.
* Cumplimiento de normas.
* Restricciones en torno al diseño o implementación.

### 2.4 Perfiles de usuario
Identifique los diversos perfiles de usuarios que usarán este producto. Los perfiles de usuario pueden diferenciarse según la frecuencia de uso, el subconjunto de funciones del producto utilizadas, la experiencia técnica, los niveles de seguridad o privilegio, el nivel educativo o la experiencia. Describa las características pertinentes de cada perfil de usuario. Ciertos requisitos pueden concernir solo a ciertos perfiles usuarios. Priorize los perfiles de usuarios de este producto para concer los requisitos que son más necesarios satisfacer.

Un actor en un caso de uso pertenecerá al menos a un perfil de usuario (podría englobar más). 

### 2.5 Suposiciones y dependencias
Enumere todos los factores asumidos que podrían afectar los requisitos establecidos en el SRS. Estos podrían incluir componentes comerciales o de terceros que planea utilizar, problemas relacionados con el entorno operativo o de desarrollo, o restricciones. El proyecto podría verse afectado si estos supuestos son incorrectos, no se comparten o cambian. Identifique también cualquier dependencia que el proyecto tenga de factores externos, como los componentes de software que pretende reutilizar de otro proyecto, a menos que ya estén documentados en otro lugar (por ejemplo, en el plan del proyecto).

### 3 Interfaces externas
Esta subsección define todos las interfazes de entrada y salida del sistema de software. Esta sección facilita la comprensión de los requisitos. Cada interfaz definida puede incluir el siguiente contenido:
* Nombre del artículo
* Fuente de entrada o destino de salida
* Rango válido, precisión y / o tolerancia
* Unidades de medida
* Sincronización
* Relaciones con otras entradas / salidas
* Formatos de pantalla / organización
* Formatos de ventana / organización
* Formatos de datos
* Formatos de comando
* Fin de mensajes

#### 3.1 Interfaces con el usuario 

Defina los componentes de software para los que se necesita una interfaz de usuario. Describa las características de cada interfaz entre el producto de software y los usuarios. Esto puede incluir imágenes de pantalla de muestra, cualquier estándar de GUI o guías de estilo de familia de productos que se deben seguir, restricciones de diseño de pantalla, botones y funciones estándar (por ejemplo, ayuda) que aparecerán en cada pantalla, métodos abreviados de teclado, estándares de visualización de mensajes de error y pronto. 

#### 3.2 Interfaces con el Hardware
Describa las características de cada interfaz entre el producto de software y los componentes de hardware del sistema. Esto puede incluir los tipos de dispositivos que deben ser compatibles, la naturaleza de los datos y las interacciones de control entre el software y el hardware, y los protocolos de comunicación que se utilizarán.

#### 3.3 Interfaces con el Software
Describa las conexiones entre este producto y otros componentes de software específicos (nombre y versión), incluidas bases de datos, sistemas operativos, herramientas, bibliotecas y componentes comerciales integrados. Identifique los elementos de datos o mensajes que entran y salen del sistema y describa el propósito de cada uno. Describa los servicios necesarios y la naturaleza de las comunicaciones. Consulte los documentos que describen los protocolos detallados de la interfaz de programación de aplicaciones. Identifique los datos que se compartirán entre los componentes de software. Si el mecanismo de intercambio de datos debe implementarse de una manera específica (por ejemplo, memoria compartida, ficheros, en la nube, etc), especifique esto como una restricción de implementación.


## 4. Requisitos
Esta sección especifica los requisitos del producto a nivel de sistema y desglosa estos en diferentes categorías. El conjunto de requisitos se debe validar y estos deben ser:
* Vigentes: Los requisitos reflejan las necesidades actuales de los usuarios del sistema, estos han podido cambiar con el tiempo, por tanto se debe revisar que sigen estando vigentes.
* Consistentes: Los requisitos no deben tener conflicto entre ellos. De tenerlo se puede establecer prioridades (obligatorio, deseable o opcional sería una opción).
* Completos: El conjunto de los requisitos define todas las funciones y restricciones deseadas por los stakeholders.
* Viables: Los requisitos pueden ser implementados dentro del presupuesto y tiempo planeado.
* Verificables: Los requisitos pueden ser comprobables (verificables) mediante tests.

Para cada requisito se debería especificar, su ID, nombre del requisito, descripción del requisito, dependencias, prioridad y justificación de su espeficación (stakeholder, derivado de un caso de uso, una interfaz necesaria, etc). Un estilo formateado facilitará la lectura. Podéis usar el siguiente formato(dependiendo de la sección se añadiran más o menos almohadillas para ponerlo en su subsección correspondiente):

### ID - Nombre del requisito
Descripción
#### Dependencias 
#### Priodidad
#### Justificación

### 4.1 Precedencia y prioridad
Esta sección está compuesta por una tabla que resumirá todos los requisitos especificados en las secciones siguientes. Se debe detallar un ID único, un nombre de requisito, su descripción, la prioridad de ese requisitos (es algo **Fundamental** a desarrollar; es **Deseable** tenerlo para que el cliente esté satisfecho; o es algo **Opcional** que estaría bien desarrollar si el tiempo lo permite), su precedencia (requisitos que deberán ser implementados antes) y el tipo (funcional o no funcional).

Esta tabla se generará en paralelo a las secciones correspondientes, y se completará cuando todas las secciones estén terminadas. Os recomiendo hacerla en excel e importarla en https://www.tablesgenerator.com/markdown_tables para generar la tabla en formato Markdown. Meter retornos de carro para que no se alarge mucho la tabla y usad la opción *_line break as <br>_* para que esos retornos de carro sean efectivos al copiarlos.


| Id 	| Nombre 	| Descripción 	| Priodidad 	| Precedencia 	| Tipo 	|
|:--:	|:----------------------------:	|:----------------------------------------------------------------------------------------------------------------------------------------------------------------:	|:-------------------:	|:-----------:	|-----------	|
| R3 	| Datos de clientes 	| El sistema deberá registar los datos de los clientes<br>para su posterior tratamiento. Estos incluirán su <br>nombre, DNI, fecha de nacimiento, género y e-mail. 	| <br>Fundamental<br> 	|  	| Funcional 	|
| R4 	| Modificar datos <br>clientes 	| El sistema permitirá modificar el e-mail del cliente. 	| Fundamental 	| R3 	| Funcional 	|
|  	|  	|  	|  	|  	|  	|
	


### 4.2 Funcionales
Esta sección especifica los requisitos funcionales de sistema que el futuro software debe tener en su entorno. Se aconseja poner un enlace al documento de casos de uso generado por magic draw para que el lector tenga una vista general de las funcionalidades del producto a generar.



### 4.3 Calidad de Servicio
Esta sección establece requisitos no funcionales relacionados con la calidad que deben presentar las funcionales del software.
 
#### 4.3.1 Rendimiento
Si existen requisitos no funcionales de rendimiento para el producto en varias circunstancias, indíquelos aquí y explique sus razones, para ayudar a los desarrolladores a comprender la intención y tomar las decisiones de diseño adecuadas. Especifique las restricciones de tiempo. Haga tales requisitos tan específicos como sea posible. Es posible que deba indicar los requisitos de rendimiento para requisitos funcionales o características individuales.

#### 4.3.2 Seguridad
Especifique los requisitos no funcionales relacionados con los problemas de seguridad o privacidad relacionados con el uso del producto. 
* Protección de los datos utilizados o creados por el producto.
* Requisitos de autenticación de identidad de usuario. 
* Políticas o regulaciones externas que contengan problemas de seguridad que afecten al producto. 
* Certificaciones de seguridad o privacidad que deben cumplirse.

#### 4.3.3 Fiabilidad
Especifique los requisitos no funcionales necesarios para establecer la fiabilidad requerida del sistema de software al momento de la entrega.

#### 4.3.4 Disponibilidad
Especifique los requisitos no funcionales necesarios para garantizar un nivel de disponibilidad definido para todo el sistema, tiempo mínimo disponible por día, máximos de reinicios permitidos por tiempo, etc.

### 4.4 Normativas aplicables
Especifique los requisitos no funcionales derivados de las normas o regulaciones existentes, que incluyen:
* Formato de informe
* Nombre de datos
* Procedimientos contables
* Seguimiento de auditoría

### 4.5 Diseño e implementación

#### 4.5.1 Instalación
Restricciones para garantizar que el futuro software se ejecutará sin problemas en la plataforma de implementación de destino.

#### 4.5.2 Distribución
Restricciones en los componentes de software para adaptarse a la estructura distribuida geográficamente de la organización en la que se va a instalar el software, la distribución de datos a procesar o la distribución de dispositivos a controlar.

#### 4.5.3 Mantenimiento
Especifique los atributos del software que se relacionan con la facilidad de mantenimiento del software en sí. Estos pueden incluir requisitos para cierta modularidad, interfaces o limitación de complejidad. Los requisitos no se deben colocar aquí solo porque son buenas prácticas de diseño.

#### 4.5.4 Reusabilidad
Software externo que deberá usarse.

#### 4.5.5 Portabilidad
Especifique los atributos del software que se relacionan con la facilidad de portar el software a otras máquinas host y / o sistemas operativos.

#### 4.5.6 Coste
Especifique las limitaciones en el costo del producto de software.

#### 4.5.7 Fecha de entrega
Especifique, si tiene, fecha de entrega del producto.

## 5. Verificación
Esta sección proporciona los enfoques y métodos de verificación planeados para calificar el software. Se recomienda que los elementos de información para verificación se proporcionen de manera paralela con los elementos de requisitos en la Sección 4. El propósito del proceso de verificación es proporcionar evidencia objetiva de que un sistema o elemento del sistema cumple con los requisitos y características especificados.


## 6. Apendices
### Apéndice A: Ejemplos de este documento relleno
Incluir y referenciar en el documento tantos apéndices como sea necesario. Los siguientes, son ejemplo de este documento (con algunas modificaciones), relleno:

[Ejemplo relleno en inglés 1](https://arxiv.org/pdf/1005.0330.pdf)
[Ejemplo relleno en inglés 2](http://www.cse.chalmers.se/~feldt/courses/reqeng/examples/srs_example_2010_group2.pdf)

### Apéndice B: Generar PDF usando un fichero MD
Hay multitud de herramientas online y offline, por ejemplo: https://www.markdowntopdf.com/
