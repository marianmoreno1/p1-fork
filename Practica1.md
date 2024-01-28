# Practica 1: Git y Github
## Marian Moreno

### 1.Git clone

**Comando:** Git Clone es un comando de Git que se utiliza para copiar (o clonar) un repositorio de Git desde un servidor remoto. En este caso, está clonando el repositorio ubicado en https://github.com/gitt-3-pat/p1.

![image](https://github.com/marianmoreno1/p1-fork/assets/123356430/df4b091c-1d60-4ef8-8535-317b67fc8ce7)

*remote: Enumerating objects: 6, done.:*  Git está enumerando los objetos del repositorio remoto, que en este caso son 6, y ha terminado de contarlos.

*remote: Counting objects: 100% (1/1), done.: Git ha contado 100% de los objetos necesarios para la operación, que en este caso era solo 1.

*remote: Total 6 (delta 0), reused 0 (delta 0), pack-reused 5:* Git proporciona un resumen de la transferencia de objetos. "Total 6" significa que hay 6 objetos en total. "Delta 0" significa que no hay diferencias en los objetos que requieren compresión. "Reused 0" indica que no se reutilizaron objetos de transferencias previas y "pack-reused 5" indica que se han reutilizado 5 objetos de packs existentes.

*Receiving objects: 100% (6/6), done.:* Git ha recibido el 100% de los objetos del repositorio remoto, que eran 6 en total.

**Resumen:** el código muestra la clonación exitosa de un repositorio de GitHub en el equipo local del usuario. Esto crea una copia local del repositorio en la que el usuario puede trabajar, realizar cambios, y luego potencialmente subir esos cambios de vuelta al repositorio remoto para que otros colaboradores puedan verlos y trabajar con ellos


### 2. Git Status

**Comando:** Este comando se utiliza para obtener información sobre el estado actual del repositorio de Git en el que se está trabajando.

![image](https://github.com/marianmoreno1/p1-fork/assets/123356430/b2782d78-d031-40b5-a3b6-7d39981b20f8)

*On branch main:* El usuario está trabajando en la rama principal llamada main.

*Your branch is up to date with 'origin/main'.:* La rama local main está actualizada con respecto a la rama main del repositorio remoto llamado origin.

*Untracked files:* A continuación, se muestra una lista de archivos que no están siendo rastreados por Git. Esto significa que son archivos nuevos o modificados que aún no han sido añadidos al sistema de control de versiones para su seguimiento.

  *(use "git add <file>..." to include in what will be committed):* Esta es una instrucción sobre cómo añadir esos archivos no rastreados al próximo commit. El comando sugerido es git add <file> donde <file> debe ser reemplazado por el nombre del archivo que se quiere comenzar a rastrear.
  
  *p1/:* Este es el directorio actualmente no rastreado. Puede ser un directorio que se ha clonado o movido recientemente en el repositorio local.
  
*nothing added to commit but untracked files present (use "git add" to track):* Git está indicando que no hay cambios en los archivos ya rastreados listos para ser confirmados (o "commit"), pero hay archivos no rastreados presentes. Sugiere usar el comando git add para comenzar a rastrear esos archivos.

**Resumen:** Se ha ejecutado git status para ver el estado del repositorio y Git ha respondido que la rama en la que está el usuario está actualizada con el remoto, pero hay un directorio p1/ que contiene archivos que aún no están siendo rastreados por Git

### 3. Git Add**

**Comando:** Se utiliza en Git para comenzar a rastrear nuevos archivos o para marcar modificaciones en archivos existentes para incluirlos en el próximo commit.
  - Rastrear archivos nuevos: Si tienes archivos que nunca has añadido al repositorio, git add los incluirá en el área de preparación (staging area), lo que significa que Git empezará a rastrear estos archivos. ("Staging" significa que estás marcando los cambios en los archivos actuales para que sean incluidos en tu próximo "commit").
  - Preparar cambios: Si modificaste archivos que ya estaban siendo rastreados, git add actualizará el área de preparación con la versión actual de esos archivos.

![image](https://github.com/marianmoreno1/p1-fork/assets/123356430/99254160-5f6c-4031-b93f-3817ecd2883b)

*warning: adding embedded git repository: p1:* Git advierte que estás intentando añadir un repositorio de Git dentro de otro, lo cual no es la práctica estándar.

*Git Add .* Al añadir el punto al comando Git Add le estás diciendo a Git que agregue al área de preparación todos los cambios (archivos nuevos, modificados, eliminados) que se encuentran en el directorio actual y en todos sus subdirectorios. (El punto se refiere a "este directorio y todos los archivos y carpetas que contiene")

**Resumen:** 
  - Agrega cambios en archivos existentes al área de preparación para el próximo commit
  - Comienza a rastrear nuevos archivos que no estaban en tu último commit
  - No afecta a los archivos que han sido eliminados
  - No incluye archivos o directorios listados en el archivo .gitignore

### 4. Git commit

**Comando:** Este comando se utiliza en Git para guardar los cambios que se preparan en el área de preparación (staging area) en el historial del repositorio (como una instantánea del estado de los archivos en ese momento). El commit guarda la configuración actual del directorio de trabajo como un nuevo commit con un ID único (un hash SHA-1).


![image](https://github.com/marianmoreno1/p1-fork/assets/123356430/ac813360-976a-4e55-a42a-4975d490e3e5)

- El parámetro -m seguido de "TU MENSAJE" permite al usuario proporcionar un mensaje de confirmación en línea, sin necesidad de abrir un editor de texto. Este mensaje es importante porque describe los cambios que se han realizado.

*[main 19014f1] TU MENSAJE:* Esta línea muestra que se ha creado un nuevo commit en la rama main. El hash del commit es 19014f1, que es un identificador único para ese commit. "TU MENSAJE" es el mensaje de confirmación que se ha proporcionado.

*1 file changed, 1 insertion(+):* Indica que hay un archivo que ha cambiado desde el último commit, y que ha habido una inserción (se ha añadido una línea).

**Resumen:** Se está confirmando la adición de un submódulo llamado p1 al repositorio actual con el mensaje de commit "TU MENSAJE"

### Git push

**Comando:** Se utiliza en Git para subir el contenido del repositorio local a un repositorio remoto. Esto incluye todos los commits hechos en las ramas locales que aún no se han subido al repositorio remoto. Sus funciones son:
 - Actualizar el repositorio remoto con los commits realizados en la rama actual.
 - Subir nuevas ramas y etiquetas al repositorio remoto.
 - Sincronizar los cambios entre el repositorio local y el remoto.

![image](https://github.com/marianmoreno1/p1-fork/assets/123356430/defd79fe-d59f-4b24-b172-90975be85f6d)

Las primeras líneas de respuesta muestran el proceso de subida.

*To https://github.com/marianmoreno1/p1-fork:* Es la URL del repositorio remoto en GitHub al que se están subiendo los cambios.

* 82add40..19014f1 main -> main:* Esto muestra el rango de commits que se están subiendo desde el último push (82add40) hasta el último commit (19014f1) en la rama main local, que ahora se está sincronizando con la rama main del repositorio remoto.

**Resumen:** La salida indica que el git push se ha completado con éxito y que los cambios locales ahora están en el repositorio remoto en GitHub

### Git checkout

**Comando:** Se utiliza  en Git para cambiar entre diferentes ramas o commits en un repositorio. También se puede usar para restaurar archivos del área de trabajo.

![image](https://github.com/marianmoreno1/p1-fork/assets/123356430/fb978625-dd10-4594-b1c6-d0bb821bcc44)

*-b feature/1:*  Crea una nueva rama llamada feature/1 y cambia a ella. La opción -b le indica a Git que cree la rama porque no existe previamente.

*Switched to a new branch 'feature/1':* Git confirma que ha cambiado a la nueva rama que acaba de crear.

![image](https://github.com/marianmoreno1/p1-fork/assets/123356430/652c6a5d-cf61-4a02-b5b7-2a0bfc5e28e5)

*Switched to branch 'main':* Git cambia del estado actual en la rama feature/1 de nuevo a la rama main.

*Your branch is up to date with 'origin/main'.:* Además, Git indica que la rama main local está actualizada con la rama main del repositorio remoto, que en este caso se asume que es origin/main.

**Nota:** Estos comandos se utilizan típicamente para trabajar en diferentes características o correcciones en aislamiento, y luego volver a la rama principal para integrar esos cambios cuando estén completos.







