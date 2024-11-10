# Git

## Configuración
### git config --global user.name "nombre_usuario"
Configura el nombre de manera global en git
### git config --global user.email "correo_usuario"
Configura el correo electronico de manera global
### git config --list
Me muestra todas las configuraciones disponibles
### git config --global core.editor "code --wait"
Configura vsc como editor de codigo para realizar los commits
## git config --global core.autocrlf
Ayuda a evitar conflictos cuando diferentes sistemas operativos como linux/mac y windows trabajan en conjunto en el mismo repositorio
### Natas :
- Existen 3 gerarquias: system, global, local las mas importantes o mas relavantes van de local hasta system.
- Puedo ver las configuraciones segun el alcanse de estas usando: git --local(system/global) --list
- El comando git config --global core.autocrlf en windows continua con true y en linux/mac con input

## Comandos basicos de git
### git init
Inicializa el repositorio
### git add
Agrega los elementos del area de trabajo al area de stage
### git status
Muestra el estado de los archivos que hay en git si estan el el stage y si estan en el area de trabajo
### git commit 
Realiza una captura de los cambios que llevamos hasta el momento subiendolos al repositorio
### Notas :
- Existen 3 diferentes areas de git las cuales son el area de trabajo, el stage y el ropositorio.
- Se pueden agregar todos los archivos de usando git . pero se recomienda colocar el nombre del archivo.
- Para agregar un mensaje al commit sin abrir el editor de codigo se le agrega -m seguido del mensaje en comillas.
- Si agregas -a al git commit podras subir todos los archivos (incluso los que no estan en stage) al repositorio

## Comandos intermedios de git
### git restore --stage nombre_archivo
Restaura los archivos que estan en el stage
### git checkout nombre_archivo
Vuelve a los ultimos cambios guardados
### git reset --hard nombre_archivo
Devuelve los elementos del area de stage(Vuelve al ultimo commit)
### git mv nombre_archivo nuevo_nombre_arhchivo
Cambia el nombre de un archivo 
### git status -s 
Forma mas corta de presentear status
### Notas :
- git checkout no funciona cuando el archivo esta en stage

## Comandos medio_avanzados de git
### git show 
Muestra todo el contenido de un archivo de un commit 
### git diff --stage 
Muestra la diferencia que hay de un archivo en stage a uno que esta en el repositorio.
### git log 
Me muestra toda la informacion de los commits echos hasta el momento
## Notas : 
- git log --oneline meustra los hast de los commits de manera recortada y los datos de los commit reducida
- git config --global core.abbrev (cantidad): Esto aumenta el numero del hast o lo disminuye
- git diff tambien nos sirve para comparar dos commits, para ello se colocan los hast de cada uno despues del git diff 

## Modificar commits
### git commit --amend 
Modifica el comentario del commit 
### git rebase -i head~ (cantidad de commits a retroseder)
Restrosede hasta un commit especifico.
### git rebase --continue
Devuelve los commits que fueron borrados al retroceder a un commit especifico.
### git reset --soft (hast del commit)
Manda el commit deseado al area de stege eliminandolo 
### git reset --mixed (hast del commit) 
Limpia el area de stage eliminando tambien el commit pero sin tocar el area de trabajo
### git reset --hard (hast del commit)
Elimina todos los cambios echos y los remplaza por los del commit seleccinado
### Notas :
- Para que los cambios actuales se agregen tambien al commit modificado se deben poner los cambios en el area de stage
- Cuando se retrocede a un commit todos los commits por delante de ese se borran.
- Simpre es mejor editar el ultimo commit
- Se pude a aceder a un commit con git --soft head~(Numero del commit) esto mueve el puntero de arriba asia abajo segun lo indicado

## Ramas
### git branch 
Revela las ramas existentes y la rama actual en la que nos encontramos
### git branch nombre-rama
Crea un nueva rama
### git checkout nombre-rama
Nos posiciona en la rama indicada
### git switch nombre-rama 
Nos posiciona en la rama indicada(Es mas recomendado hacer esto que hacerlo con checkout)
### git checkout -b nombre-rama
Crea una rama y nos mueve al mismo tiempo a la rama creada
### git switch -c nombre-rama 
Crea una rama y nos mueve al mismo tiempo a la rama creada
### git branch -d nombre-rama
Elimina una rama especificada 
### git branch -m nombre-rama nuevo-nombre
Modifica el nombre de una rama especificada(Solo hacer esto si no estamos en la rama que deseamos modificar)
### git branch -m nombre-rama
De esta manera se modifican 
### git merge rama-combinar
Junta dos ramas
### Notas : 
- git branch nombre-rama crea una rama pero nosotros seguimos en la rama en la anterior
- Se recomienda crear una rama desde la rama principal 
- Se puede crear una rama de la rama
- Se recomienda usar switch para moverse y crear ramas
- No! debemos estar en la rama que deseamos borrar para borrarla
- Se pueden desacer la fucion de una rama eliminado el commit donde se funcionaron
- Para combinar dos ramas debemos estar en la rama que deseamos combinar

## .gitignore
Es un archivo que evita que se suban siertos archivos o cambios al repositorio
### Nota:
- Revisar el documento .gitignore para mas informacion
- Se puede configurar un .gitinore_global para que se ingonore un archivo especifico de todos mis repositorios tiempo 2:25:57

## Alias
Simplifica comandos de git
## git config --global alias.(nombre-nuevo-comando) 'comando'

## git reflow

