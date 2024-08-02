# Clase 02 - Git desarrollo colaborativo

## Repasando dinamica de trabajo base de git

## listar una cantidad especifica de commits en el log

git log --oneline <cantidad-commits>
git log --oneline -5

### Haciendo un commit. Pasos


1. hacer un status para ver en que estado estan los archivos que quiero sean parte del commit

2. Agregar lo que quiero dentro del commmit al área de confirmación (stating area)

git add <nombre-archivo>
git add clase02/readme.md
git add # agregar todo lo que sea parate de la funcionalidad en la que trabajo

3. Hago el commit. Todo lo que estuviera en el area de stating se guarda en el repositorio local

git commit -m "nuevo commit, mensaje descriptivo"

## git diff comparo entre diferentes commits en el tiempo

git diff <hash> <hash>
git diff 6ceff27 376047e

## Para agregar algo que olvide o quiero incorporar en el ultimo commit, uso el sig comando  Agregar cosas al ultimo commid o modificaciones
git add .
git commit --amend --> se abre el nano y podemos modificar el mensaje. Tambien podemos agregar un contenido al ultimo commit si es que nos olvidamos o queremos agregarle






## RAMAS (branches)

## Ver los listados en orden de los commits
git log --oneline --all --graph --decorate


## Nos permite trabajar en el proyecto de manera auxiliar

git add --patch -> elegimos que guardar y que no

## diferencias entre el stage area y local re

git diff --storage



## Listar ramas 

git branch

#crear una rama

git branch <nombre-rama>
git branch "navbartrabajo"



## cambiar de ramas

git switch <nombre de la rama>

## ver que va sucediendo entre ramas

git branch -v

## Borrar rama ( NO HAY QUE ESTAR PARADO EN LA MISMA RAMA QUE QUEREMOS BORRAR)

git branch -d <nombre-rama> - si estamos seguros de borrarla, cambiamos la -d por -D ( D mayuscula) -> si el contenido de la rama que voy a borrar no esta en ningun otra rama, me va a pedir confirmacion.


## Fusiones (merge) de ramas (branches)

git merge <nombre-rama>

"si quiero traer el contenenido a MAIN, tengo que estar parado en MAIN"

## Para abortar el merge --> 
merge --abort


## DIFERENTES FUSIONES

* Fusion --> fast-forward (automatico)
* Fusion --> tres vias (automatico) (genera un comit intermedio entre los ultimos comits de las ramas involucradas)
* Fusion --> Manual (Git no puede solocionar el conflicto) pide que yo como desarrollador solucione el conflicto