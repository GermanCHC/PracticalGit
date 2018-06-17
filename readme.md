#Ejercicio 1
* ¿Qué comando utilizaste en el paso 11? ¿Por qué?
git reset --hard HEAD~1. Me pareció la forma más rápida de desplazarme un paso atrás de forma lineal en la rama en la que estaba. Deshaciendo cambios en el staging area.

* ¿Qué comando o comandos utilizaste en el paso 12? ¿Por qué?
git reset --hard HEAD@{1} Porque es la forma más rápida. Si ha habido otros commits buscaría la forma de recuperarlo con el reflog.

* El merge del paso 13, ¿Causó algún conflicto? ¿Por qué?
No. Porque la rama master no tenía ningún commit intermedio que pudiera generar conflictos al incorporar algún cambio a styled.

* El merge del paso 19, ¿Causó algún conflicto? ¿Por qué?
Sí. Porque la rama htmlify cambio muchas lineas del archivo.

* El merge del paso 21, ¿Causó algún conflicto? ¿Por qué?
No. Porque ha sido un Fast-Forward. Es decir, los cambios de la rama styled están hechos desde master, con lo que para master solo se mueve hacia delante incorporando los nuevos cambios.

* ¿Qué comando o comandos utilizaste en el paso 25?
$ git log --graph --pretty=oneline
* El merge del paso 26, ¿Podría ser fast forward? ¿Por qué?
Si. Porque lo único que se hace es incorporar los cambios a la rama padre, con lo que haría Git es mover el HEAD hacia delante.
* ¿Qué comando o comandos utilizaste en el paso 27?
git reset HEAD@{1}

* ¿Qué comando o comandos utilizaste en el paso 28?
git reset --hard

* ¿Qué comando o comandos utilizaste en el paso 29?
git branch -D title

* ¿Qué comando o comandos utilizaste en el paso 30?
git reflog (Para encontrar el commit anterior al momento en que fui a master para borrar title)
git checkout d6d51e1(num_commit)
git checkout -b title (para crear rama title de nuevo conservando los cambios del commit detached)
git checkout master
git merge title

* ¿Qué comando o comandos usaste en el paso 32?
git log (para obtener el commit inicial)
git checkout 750613f5736ddc9d3838e12ebfe83478b049c3fd (para ir al commit inicial)
git reset HEAD (para desplazar al HEAD a este commit)

* ¿Qué comando o comandos usaste en el punto 33?
git checkout master(para desplazar HEAD al ultimo punto de master, que es el final. En caso de haber borrado master hubiera buscado con el reflog) 