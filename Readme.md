# Clase 01 - Desarrollo colavorativo con git

## Configuraciones iniciales de la herramienta

### Agrego un usuario y un correo --> este usuario y el correo va a ser utilizado para firmar cada una de las intantaneas (fotos/commits). Es obligatorio la configuracion de usuario y correo


diegoi  q



Clase 01 - Desarrollo Colaborativo GIT
Configuraciones iniciales de la herramienta
Agrego un nombre de usuario y correo
Este usuario y el correo va a ser utilizado para firmar cada una de la instantaneas (fotos/commits). Es obligatorio la configuración de este usuario y correo.

git config --global user.name "Maximiliano Principe"
git config --global user.email mlapeducacionit@gmail.com
git config --local ... #Tiene que existir un repositorio para poder 
git config --system ...


git config --get-regexp user
# ----
user.name Maximiliano Principe
user.email mlapeducacionit@gmail.com


Borrar alguna de las configuraciones
git config --global --unset user.mail


Modificar el editor de texto que usa GIT
git config --global core.editor "nano"


Quieren cambiar la rama por defecto. Es master a Main
git config --global init.defaultBranch main
Empezando a trabajar con GIT
git init


Nota: Este comando crear un repositorio de git en la carpeta actual. O sea crea un directorio oculto llamado .git (donde dentro tengo los archivos del repositorio)

Controlar el status de los archivos dentro del repositorio
git status



Areas posibles en las que pueden estar los archivos
Working Directory (Directo de trabajo) donde van agregando, borrando al archivo el desarrolllo

Staging Area (Area de control de cambios) Se agregan los archivos para darle seguimiento y posteriormente sacarles una foto (commit)

Local Repo (Area de validación de cambios, donde se registran las modificaciones realizadas) Donde van a estar todas las fotos (commit) que vaya sacando.

Estados de los archivos
Untracked (Sin seguimiento) => archivos que no se agregaron al index/stage y por consecuente no se les da seguimiento.
Staged => Archivos que fueron agregados al index/stage area y cuyos cambios van a ser incorporados al repositorio
Unmodified => Archivos que se cuentran en en el respositorio y no fueron modificado (Con respecto al repositorio)
Modified => Archivos que se encuentro en el repositorio pero difieren con lo que se encuentra actualmente en el directorio trabajo (Working directory)
Agregar al area de Staging
Marca el archivo y los cambios para que formen en un futuro parte de la siguiente instantenea (foto/commit).

git add <nombre-archivo>
git add clase.01/README.md
git add . #


Guarda en el repositorio una instantanea. Sacar una foto/commit
git commit -m "Mensaje descriptivo de lo que se hizo"


Para comparar el Working Directory y el Local Repo
git diff


Areas del repositorio de GIT
![Alt text](image.png)

Quitar de la area de staging area
git restore --staged <nombre-del-archivo>
git restore --staged clase.01/README.md


Como ver lo que paso en un commit
git show <hash>
git show 60776


Mostrar el historico de commit
git log # Version larga.
git log --oneline # Version resumen


.gitignore: Para ignorar archivos que no deseo que esten en el repositorio
Creo normalmente en el directorio raíz del proyecto el archivo .gitignore

.gitkeep: Para darle seguimiento a carpetas vacias
Porque git no le da seguimiento y guarda en el repositorio (LR) las carpetas vacías