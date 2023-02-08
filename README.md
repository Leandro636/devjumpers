Paso a paso, Ejercitación final
1) En primer lugar cree el repositorio en GitHub. Copiada la ruta, utilize Git clone para bajarlo a mi repositorio local. 
2) Ingrese a la carpeta desde mi repositorio, con cd devjumpers; Cree el archivo README.md utilizando el comando touch README; Añadi los cambios con git add . y realizé el primer commit "commit inicial"; Por último, subí los cambios al repositorio remoto con git push.
3) Cree el archivo llamado "privado.txt" utilizando touch, y mkdir "privada" para crear la carpeta; también cree el archivo .gitignore y dentro de él escribí las rutas a los archivos que quería ocultar, la carpeta privada, y "privado.txt" en este caso.
4) Añadí el archivo 1.txt al repositorio local con touch 1.txt. 
5) Git status para chequear, y git add . para poder pushear el progreso.
6) Cree la rama v0.2, utilizando el comando git checkout -b "v0.2" porque me posiciona directamente en la rama creada para trabajar. Añado el fichero con touch. Reviso con git status, añado los cambios con git add . y posteriormente git push para actualizar el repo remoto (git push --set-upstream origin v0.2)
7) Regreso a la rama main con git checkout main, para realizar el git merge con la rama v0.2. 
8) Con el comando echo "Hola" >1.txt añado texto al archivo, y lo comiteo. 
9) Con git checkout regreso a la rama v0.2 y repito el proceso para añadir "Adios". 
10) Git merge v0.2 desde la rama main, y me encuentro con el conflicto.

<<<<<<< HEAD
Hola
=======
Adios
>>>>>>> v0.2

Reviso con git branch --merged para ver las ramas fusionadas (main), y con git branch --no-merged (v0.2) para revisar las que no se fusionaron.

11) Arreglo el conflicto con el bloc de notas, y con git add . y commit guardo los cambios y merge en main para que se guarde. Reviso con git branch --merged y --no-merged si la fusion fue correcta. 

12) Con git branch -D v0.2 elimino la rama en la estuve trabajando. 

Cambios: 
 git  log --oneline --decorate --all --graph
*   061d434 (HEAD -> main) Conflicto Solucionado
|\
| * d84fa8c Agregado Adios
* | bc40550 Agregado Hola
|/
* c05b48a (origin/v0.2) Nueva rama v0.2
* ca7eb9a (origin/main) gitignore; 1.txt creados
* 090f833 Commit inicial

| NOMBRE | GITHUB | 
| ------ | ------ |
| Ivan       | https://github.com/ivandelaparte |
| Arrmando       | https://github.com/ArmaTQ  |
| Leandro | https://github.com/leandro-cuevas |
