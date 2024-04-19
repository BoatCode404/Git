#  Para convertir una carpeta en un nuevo proyecto Git
 ```bash
 git init
````
Algo como esto debería aparecer a continuación:

Initialized empty Git repository in /Users/username/.git

Esto significa que se creó el proyecto Git.

Para conectar el repositorio creado localmente con uno que creamos en GitHub, podemos usar el remote addcomando:

git remote add origin https://github.com/username/repo-name.git 

Para definir la rama principal, que será la rama a la que enviaremos el código . ¡Discutiremos qué ramas hay más adelante en el capítulo!

git branch -M main
