# Linea de comandos operaciones básicas

---

## *¿Que es Consola de comandos/ terminal?*

Es el programa que recibe los comandos escritos que le envías directamente al sistema y te entrega una respuesta.
Es una forma directa de interactuar con un sistema de forma comprensiva para el humano, pero con un nivel de abstracción bajo

## *¿Porque aprender a usarla?*

- Interaccion directa con el sistema
- Cortita y al pie, el sistema ejecuta y responde lo que explícitamente le pedís
- Velocidad de respuesta
- Ante desastres el primer punto de interaccion entre tu hardware, datos y vos es la consola

---
---

## **Operaciones básicas.**

- ### *Gestión de archivos*

- ### *Visualization de archivos de texto .conf .log etc*

- ### *Diagnostico de red*

- ### *Procesos y servicios*

---
---

## **Conceptos básicos necesarios para utilizar la consola correctamente**

### Rutas

- Absolutas: las rutas absolutas comienzan desde la raíz del sistema

> Suponiendo que estamos en la carpeta del usuario
> Windows: C:\Usuarios\dmori\Escritorio\contadores.xls
> Linux: /home/dmori/Escritorio/contadores.xls

- Relativas: las rutas relativas comienzan desde el punto en el que estamos parados en el momento.

> Suponiendo que estamos en la carpeta del usuario
> Windows: \Escritorio\contadores.xls
> Linux: ~/Escritorio/contadores.xls

- Directorios especiales
Directorio actual . (donde estamos parados)
Directorio padre .. (el directorio inmediatamente superior)
Directorio personal (~)(Linux)

### Sintaxis de comandos

- Comando: Accion/funcion que vamos a ejecutar
- Argumento: objetivo
- opciones o bandera: aclaraciones que modifican el comportamiento del comando

> | comando | bandera|Argumento|
> |---------|--------|---------|
> | ping    | -t     | 8.8.8.8 |

---
> En el ejemplo hacer un ping(comando) -t(bandera para que no termine solo) a 8.8.8.8 (argumento/destino)

### Redirecciones y pipes

- Redireccion: guardar la salida de un comando en un archivo

> ls -l > salida.txt (listamos el contenido de nuestra ubicación y creamos un archivo .txt con el resultado)

- Pipes (tuberías): enviamos el resultado de un comando a otro

> ls -l | grep raz (listamos el contenido de nuestra ubicación y en el resultado buscamos coincidencias con la palabra raz)

## *Comandos básicos y sus alternativas en windows y Linux*

| Windows | Linux | Descripción |
|----------|----------|-------------|
| `dir` | `ls -l` | Listar directorios y archivos |
| `ren` | `mv` | Renombrar un archivo |
| `copy` | `cp` | Copiar un archivo |
| `move` | `mv` | Mover un archivo |
| `cls` | `clear` | Limpiar la pantalla |
| `del` | `rm` | Eliminar un archivo |
| `fc` | `diff` | Comparar contenidos de archivos |
| `find` | `grep` | Buscar una cadena en un archivo |
| `sort` | `sort` | Ordenar lineas de texto alfabéticamente |
| `comando /?` | `man comando` | Mostrar ayuda del comando |
| `cd` o `chdir` | `pwd` | Mostrar el directorio actual |
| `time` | `date` | Mostrar la hora y fecha |
| `cd` | `cd` | Cambiar el directorio actual |
| `md` o `mkdir` | `mkdir` | Crear un nuevo directorio |
| `echo` | `echo` | Imprimir texto en pantalla |
| `notepad` | `nano` | Editar archivos de texto |
| `type archivo.txt` | `cat archivo.txt` | Mostrar el contenido de un archivo |
| `more archivo.txt` | `less archivo.txt` | Visualizar archivos extensos página por página |
| `exit` | `exit` | Salir de la terminal |
| `rmdir` | `rmdir` | Eliminar un directorio vacío |
| `rmdir /s` | `rm -rf` | Eliminar un directorio y su contenido |
| `taskkill` | `kill` | Terminar un proceso |
| `tasklist` | `ps aux` | Listar procesos en ejecución |
| `set` | `export` | Establecer variables de entorno |
| `ping` | `ping` | Verificar conectividad con un host |
| `nslookup` | `nslookup` | Consultar registros DNS |
| `tracert` | `traceroute` | Mostrar la ruta de los paquetes hacia un host |
| `ipconfig` | `ip addr` / `ifconfig` | Mostrar la configuración de red |
| `ipconfig /all` | `ip addr` / `ifconfig` | Mostrar información detallada de las interfaces de red |
| `netstat -ano` | `ss -tulpn` / `netstat -tulpn` | Mostrar conexiones y puertos abiertos |
| `hostname` | `hostname` | Mostrar el nombre del equipo |
| `whoami` | `whoami` | Mostrar el usuario actual |
| `curl` | `curl` | Realizar consultas HTTP/HTTPS |
| `systeminfo` | `uname -a` | Mostrar información general del sistema |
| `systeminfo` | `cat /etc/os-release` | Mostrar información de la distribución o sistema operativo |

---
---

### *Actividad*

---
Vamos a jugar un poco, tenes que completar una mision para empezar
tenes que clonar este repo <https://github.com/Miracl3nb/ordenes.git>
moverte a la carpeta y empezamos

---
### *Actividad para casa*

Wargames

tenes que completar hasta el nivel 5 inclusive de los wargames de overthewire recopila las capturas de las claves y el método que usaste para conseguirlas

<https://overthewire.org/wargames/bandit/>

