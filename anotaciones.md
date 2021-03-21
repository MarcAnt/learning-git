# Anotaciones de Aprendiendo git y github de https://www.youtube.com/watch?v=3fUbBnN_H2c

Regresar un archivo del staging area: 

`git rm --cached index.html`

Regresar todos los archivos del staging area: 

`git rm -r --cached .`

Para obtener los hash de los commits que se han hecho: 

`git log`

Para ver los cambios que se han hecho: 

`git diff`

Para deshacer cambios: 

`git restore`

Cambiar el comentario del último commit: 

`git commit --amend -m "added body selector to main.css"`

Obtener todos los branch remotos:

`git branch -r`

Todos los ramas o branches: 

`git branch -a`

Crear una rama o branch: 

`git branch xxxx-xxx`

Crear a la rama main: 

`git checkout -`


Cambiar entre ramas o braches: 

`git checkout xxxx-xxx`
