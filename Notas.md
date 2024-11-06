# Git Hup

## Configuración

### git config --global user.name ""
Configura el nombre de manera global en git

### git config --global user.email ""
Configura el correo electronico de manera global

### git config --list
Me muestra todas las configuraciones disponibles

### git config --global core.editor "code --wait"
Configura vsc como editor de codigo para realizar los commits

## git config --global autocrlf
Ayuda a evitar conflictos cuando diferentes sistemas operativos como linux/mac y windows trabajan en conjunto en el mismo repositorio

### Natas:
- Existen 3 gerarquias: system, global, local las mas importantes o mas relavantes van de local hasta system.
- Puedo ver las configuraciones segun el alcanse de estas usando: git --alcance --list
- El comando git config --global autocrlf en windows continua con true y en linux/mac con input

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

## Comandos bascios de git

### git restore 
Restaura los archivos que estan en el stage

### git checkout nombe_archivo
Vuelve a los ultmos cambios guardados

### git reset --hard nombre_archivo
Devuelve los elementos del area de stage(Vuelve al ultimo commit)

### git mv nombre_archivo nuevo_nombre_arhchivo
Cambia el nombre de un archivo 

### git status -s 
Forma mas corta de presentear status

### Notas :
- git checkout no funciona cuando el archivo esta en stage