# Sistemas Operativos

---

## *¿Que es un sistema operativo?*

Es el software que gestiona los recursos físicos de un sistema computacional (computadoras, celulares, routers, cámaras, dvrs, nvrs etc)

Se lo podría simplificar a un conjunto global de software coordinado para controlar los recursos y servir a la operación computacional  

## *Funciones base de un sistema operativo*

- Asignar y administrar la memoria ram entre los diferentes procesos  
- De ser necesario organiza los estados de almacenamiento  
- Coordina y prioriza las tareas del CPU  
- Gestiona la comunicación con HW interno como externo(por medio de los drivers)
- En la mayoría de los casos proporciona al usuario una interfaz gráfica o consola de comandos con la cual operar y recibir outputs (No excluyente)

---
---

## **Tipos de sistemas operativos**

### *Desktop*

- Ofrece un entorno gráfico y sistema de ventanas  
- Suelen ofrecer más opciones de personalización en un entorno controlado
- Mantienen el uso del sistema y recursos en una capa elevada de abstracción

>EJ: Windows, Ubuntu, Mac Os y SteamOs

### *Server de propósito general (de forma generalista)*

- Ofrece estabilidad y rendimiento optimizando el uso de recursos físicos
- Multi-user, admiten múltiples conexiones simultaneas
- Nivel de abstracción medio en versiones Windows, bajo en Linux
- Herramientas pre fabricadas o preparadas en compatibilidad para ofrecer servicios  
- Cifrados mas robustos  

> EJ: Windows Server, RedHat 10, Oracle 8  

### *Sistemas especializados / appliances*

- Preparados para ambientes y propósitos específicos
- Optimizados funcionar mejor en un rol especifico  

>EJ: Proxmox (base debian con propósitos de ser un hipervisor bare-metal)
TrueNAS (Almacenamiento)
AsteriskPBX (SO base linux para gestionar centrales telefónicas y troncales de telefonía)

### *SO Embebidos*

- SO de propósito dedicado  
- Sistemas cerrados  
- En muchos casos sin dar output directo a usuarios  
- Gestionan hardware limitado
- En muchos casos no permiten,administración directa o están altamente limitados en acceso.

> EJ: Swicths, tvs, algunos electrodomésticos  

---
---

## **Utilidades de SO Servidores.**

 En los servidores existen los servicios, softs de propósito especifico  

- Manejo de sesiones simultaneas encapsuladas por usuario
- Administrar contextos de red  
- Servir recursos/carpetas/archivos remotamente a través de la red
- Gestionar dispositivos de la red
- Hostear y exponer aplicaciones y web a internet
- Virtualization  
- Gestión de usuarios y políticas centralizada
- Manejo de logs y auditoría  
- Alta disponibilidad
- Backups y recuperación
- etc

Los servicios también suelen tener características que se pueden adicionar  

>por ejemplo al servicios de IIS (servidor web de Microsoft) se le puede agregar la característica de SMTP (protocolo utilizado para enviar mails) y levantar un servidor de mail  

Los sistemas operativos para servidor más utilizados son Linux (para generalizar) Y Windows  

Windows se utiliza en entornos más corporativos robustos , para onpromise y servicios de gestión  

Linux para propósito general, web, cloud, micro servicios y entornos corporativos más livianos

Para la mayoría de los servicios de un so existen alternativas en el otro  

Algunos ejemplos

|Servicio|Funcion|SO|
|---|---|---|
|IIS |Servidor| Web |Windows|
|APACHE|Servidor Web|Linux / Windows|
|NGINX|Servidor Web |Linux / Windows|
|MS Sql|Motor base de datos relacional|Windows|
|MySql|Motor base de datos relacional|Linux / Windows|
|MariaDB|Motor base de datos relacional|Linux / Windows|
|Hyper-V|Virtualización|Windows|
|Proxmox|Virtualización|Linux|
|VMWare|Virtualización|Linux / Windows|
|Active Directory|Directorio de usuarios, equipos de red, Gestion de GPO ETC|Windows|
|Samba AD DC|Directorio de usuarios y equipos de red|Linux|
|FREEIPA|identidad/autenticación tipo LDAP/Kerberos|Linux|

---
---

## *Diferencias basicas entre windows y Linux (Ultra basicas super generalistas)*

Windows y linux, hacen prácticamente lo mismo administran recursos y ejecutan aplicaciones  

Pero están pensados desde aristas diferentes con objetivos principales distintos por **filosofía**

En este momento voy a recalcar solo algunas diferencias  

>**El sistema de archivos**

En Windows cada disco es "independiente" c:\  d:\  se maneja con rutas más visuales  

![Arbol de directorios Windows](../Assets/Arbol%20de%20directorios%20Windwos.png)

En linux todo cuelga de una única raíz, no existen letras de disco separadas, las unidades de "montan"
Dentro del sistema TODO FORMA PARTE DEL MISMO ARBOL

![Arbol de directorios Linux](../Assets/Arbol%20de%20direcotios%20Linux.png)

>**Instalación de Software**

En Windows, la forma más común es descargar el ejecutable .exe .msi y lo instalar manualmente con algunos clicks y cada soft de gestiona por separado

El Linux se usan repositorios externos y gestores de paquetes por consola por medio de un comando
Por ejemplo  ***sudo apt install nginx***.

este comando le dice a "apt" gestor de paquetes que busque en los repositorios

Nginx y lo instale el sistema deja listo el soft al terminar  

Existen actualmente alternativas graficas que lo hacen muy similar a windows por ejemplo flatpack o las propias tiendas

De la distribuciones (distribuciones -> algo asi como el sabor de linux que elegís)

>**Permisos y usuarios**

En windows se usan ACLs y se gestionan por la GUI

En LINUX TODO tiene permisos asociados o podes ponerle permisos específicos (lectura, escritura y ejecucion)
Lo que lleva a un concepto interesante
***EN LINUX  CASI TODO ES UN ARCHIVO***  

En linux las configuraciones, dispositivos, procesos, logs son considerados archivos y pueden ser manejados como tal  

Por ejemplo  

/etc/nginx/nginx.conf -> config
/var/log/syslog -> logs
/dev/sda -> disco
/dev/sda01 -> disco  | partición de sda
/dev/sdb -> disco
/dev/sdb01 -> disco | partición de sdb
/dev/sdb02 -> disco | partición de sdb

En windows todo esto está más abstraído usas gui y el registro

>**Administración**

Windows esta más orientado a la interfaz gráfica, herramientas visuales y powershell (terminal supero potente de ms)
Se podria decir que todo un poco más limitado la mayoría del control del sistema lo tiene el propio sistema

Linux tiene una fuerte uso de terminal, automatización más natural y un control más directo de desearlo
OJO no todo es consola y escribir comando para prender la wifi tenes la chance de usarlo mas simple

Pero en caso de querer o tener que tocar el sistema de forma mas profunda podes hacerlo.

Esto es super resumido mas adelante vemos en profundidad

---
---

## *Para completar Juntos*  

Servicios y características reales utilizadas en RAZ

**AD DS** -->  Manejar y registrar los dispositivos / usuarios de red politicas de administración

**DHCP** -->  Manejar el pool de asignación de ip rotativas, gestionar el tiempo en el que se renueven, mantiene el acceso a la red de los dispositivos, ademas de reservar ip especificas que se requerian

10.1.0.1  ---> 10.1.0.254

>**Pool DHCP**

Especifica el rango de ip que se van a asignar temporales por dhcp

>**DNS** -> Requerido para ambiente de DHCP controlado se encarga dar reconocimiento a los equipos de red  

Relacionando IP numéricas a Identificadores alfanuméricos de los dispositivos (nombres, mac addresses)

>**IIS** -> Web server de microsoft  --> esta en servidor VIN

En raz lo utilizamos para hostear las web internas y anteriormente API de aplicaciones móviles  

>**Acceso Remoto** --> Crear y gestionar vpn privada de tipo SSTP para servidores o usuarios muy específicos
>**File Server** --> esta en servidor VIN  

Compartir una carpeta o disco del sistema con la particularidad de podes gestionar permisos y roles

>**Servicio de Escritorio remoto** -> esta en TRELLES server

Servir y conmutar las sesiones remotas a través de los ThinClient  

Logeo de usuario -> registro de dispositivo de acceso ->numero de session -> Procesos asociados a numero de session encapsulados para evitar conflictos

---
---

### *Actividad*

---
Teniendo en cuenta los charlado, si hipotéticamente se apagan todas las virtuales de Trelles,
y por limitaciones técnicas no podemos iniciar todas las vms  

¿Cuáles iniciaríamos para proporcionar operatividad general?
¿Cuál es orden de dependencia directa entre los servicios de la infraestructura de Trelles? Justificar la respuesta

---
Exposición a presentar  

Tomando lo visto como referencia lo visto y la información que puedas recopilar por internet tenes que exponer sobre estos dos servicios SERVICIO DE IMPRESIÓN|Print Server (windows) y NFS Network File System (Linux)

Tenes que poder exponerme:

¿para qué sirven? ¿cómo funcionan? ¿Puede ser implementado en Raz?  ¿Qué mejoras traería? ¿Cuáles son los requisitos?

No necesito que me des una explicación técnica profunda sobre los protocolos, que seas un experto en el tema ni que puedas implementarlo vos, es obvio que te van a faltar conocimientos, con que puedas responder las preguntas y me lo puedas explicar con tus palabras es suficiente

No más de 10 min por servicio
