# Roadmap Bash para DevOps

## Conceptos

 *Terminal Linux*
 - Shell
 - Variables
 - Expansiones

        shell
	      :es la terminal que se utiliza para interactuar directamente con el s.o de forma eficiente y lo mas directa posible existen motores de terminal como bash y sh

 ---
        variables
        :        

  > ### Estado
  > - [ ] Me siento cómodo explicándolo
  > - [ ] Lo usé en un laboratorio
  > - [ ] Lo usé en un caso real
 ---
 *Navegación*
 - pwd
 - ls
 - cd
 - tree

        pwd
        : pwd muestra el directorio en el cual esta posicionado

 ---
        ls
        : ls lista el contenido del directorio indicado si no indico directorio usa la posicion actual.
        ls -a lista archivos y los archivos ocultos 

---
        cd
        : cd se usa para moverse entre directorios 
        para indicar que desamos cambiar a un directorio dentro del mismo directorio se indica con "." cd ./notas/ por lo contrario si queremos ir al directorio padre se indica .. cd .. > nos manda al direcotio superior cd ../python > nos manda al direcotio python dentro del directorio superior

---
        tree
          :muestra una lista estructurua de los directorios y archivos en forma de arbol
        

  > ### Estado
  > - [ ] Me siento cómodo explicándolo
  > - [ ] Lo usé en un laboratorio
  > - [ ] Lo usé en un caso real
 ---
 *Manipulación de archivos*
 - cp
 - mv
 - rm
 - mkdir
 - touch
---
       cp
       : cp se utiliza para copiar archivos o directorios de una ubicación a otra sin modificar ni eliminar el archivo original.	   
---
       mv
       : mv se utiliza para mover archivos o directorios de una ubicación a otra.
	   
---
       rm
       : rm se utiliza para eliminar archivos o directorios de forma permanente desde la terminal.
	   
---
       mkdir
       : mkdir se utiliza para crear uno o varios directorios en la ubicación indicada.
	   
---
       touch   
       : touch se utiliza para crear uno o varios archivos vacíos.
	   

 ```bash
ls ../notas/

 ```


  > ### Estado
  > - [ ] Me siento cómodo explicándolo
  > - [ ] Lo usé en un laboratorio
  > - [ ] Lo usé en un caso real
  
 ---
 
*Lectura de información*
 - cat
 - less
 - head
 - tail
---
       cat
       : cat se utiliza para mostrar el contenido de uno o varios archivos.
	   
---
	   less
       : less se utiliza para visualizar el contenido de un archivo página por pagina, permitiendo desplazarse.
	   
---
	   head
       : head se utiliza para mostrar las primeras lineas de un archivo. Por defecto, muestra las primeras 10.
	   
---
	   tail 
       : tail se utiliza para mostrar las ultimas lineas de un archivo. Por defecto, muestra las ultimas 10.
	   
---
  > ### Estado
  > - [ ] Me siento cómodo explicándolo
  > - [ ] Lo usé en un laboratorio
  > - [ ] Lo usé en un caso real

---
 *Búsqueda*
 - grep
 - find
 - locate
 - which

---
       grep
       : grep se utiliza para buscar palabras dentro de uno o varios archivos, mostrando las lineas que contienen la coincidencia.
---
       find
       : find se utiliza para buscar archivos o directorios dentro de una ubicación, utilizando criterios como el nombre, el tipo o el tamaño.
---
       locate
       : locate se utiliza para buscar archivos o directorios por su nombre.
---
       which
       : which se utiliza para mostrar la ruta donde se encuentra un comando o programa ejecutable disponible en el sistema.
---
  > ### Estado
  > - [ ] Me siento cómodo explicándolo
  > - [ ] Lo usé en un laboratorio
  > - [ ] Lo usé en un caso real

---
*Procesamiento de texto*
- cut
- sort
- uniq
- tr
- sed
- awk

---
       cut
       : se utiliza para extraer columnas o caracteres especificos de un archivo.
---
       sort
       : sort se utiliza para ordenar lineas de texto de forma alfabetica o numerica.
---
       uniq
       : uniq se utiliza para eliminar lineas duplicadas de un archivo o texto.
---
       tr
       : tr se utiliza para reemplazar, eliminar o transformar caracteres de un texto.
---
       sed
       : sed se utiliza para buscar, reemplazar o modificar texto de forma automatica.
---
       awk
       : awk se utiliza para procesar, analizar y extraer información de archivos o textos organizados en columnas.
---
  > ### Estado
  > - [ ] Me siento cómodo explicándolo
  > - [ ] Lo usé en un laboratorio
  > - [ ] Lo usé en un caso real

---
*Redirecciones*
- ">"
- ">>"
- "<"
- "2>"
- Pipes

  > ### Estado
  > - [ ] Me siento cómodo explicándolo
  > - [ ] Lo usé en un laboratorio
  > - [ ] Lo usé en un caso real

---
*Procesos*
 - ps
 - top
 - htop
 - kill
 - jobs
 - bg
 - fg
---
       ps
       : ps se utiliza para mostrar información sobre los procesos que se están ejecutando en el sistema.
---
       top
       : top se utiliza para monitorear los procesos del sistema, el uso de CPU, memoria, etc.
---
       htop
       : aaaaa
---
       kill
       : kill se utiliza detener la ejecución de un proceso.
---
       jobs
       : jobs se utiliza para mostrar los procesos que se estan ejecutando en segundo plano o que fueron suspendidos.
---
       bg
       : bg se utiliza para reanudar un proceso suspendido y continuar su ejecución en segundo plano.
---
       fg
       : fg se utiliza para traer un proceso del segundo plano al primer plano.
---
  > ### Estado
  > - [ ] Me siento cómodo explicándolo
  > - [ ] Lo usé en un laboratorio
  > - [ ] Lo usé en un caso real

 ---
*Scripting*
  - Variables
  - Condicionales
  - Bucles
  - Funciones
  - Parámetros

  > ### Estado
  > - [ ] Me siento cómodo explicándolo
  > - [ ] Lo usé en un laboratorio
  > - [ ] Lo usé en un caso real
  ---
*Administración*
  - systemctl
  - journalctl
  - cron
  - permisos Linux
  > ### Estado
  > - [ ] Me siento cómodo explicándolo
  > - [ ] Lo usé en un laboratorio
  > - [ ] Lo usé en un caso real


---
*Objetivo final*
 - Automatizar administración Linux
 - Crear scripts reutilizables
 - Resolver problemas desde consola



## Prácticas
- [ ] ...

## Laboratorios
- [ ] ...


