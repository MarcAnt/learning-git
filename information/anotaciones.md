# Anotaciones de Aprendiendo git y github de <https://www.youtube.com/watch?v=3fUbBnN_H2c>

Configurar git globalmene

```bash
    git config --global user.name MarcAnt
    git config --global user.email @mail.com
```

Cambiar el nombre a una rama. Ejemplo de cambiar de master a main

`git switch -c main`

Regresar un archivo del staging area:

`git rm --cached index.html`

Regresar todos los archivos del staging area:

`git rm -r --cached .`

Para obtener los hash de los commits que se han hecho en una rama:

`git log`

Para obtener todos los hash de los commits que se han hecho:

`git log --branches='*'`

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

Eliminar una rama:

`git branch -D xxxx-xxx`

Crear a la rama main:

`git checkout -`

Cambiar entre ramas o braches:

`git checkout xxxx-xxx`

Crear la nueva rama en github:

`git push -u origin xxxx-xxx`

Para crear y cambiar de una vez entre ramas:

`git checkout -b x-xxxx`

Para eliminar una rama (debes estar en la rama principal para hacerlo):

`git branch -d x-xxxx`

Para unir entre ramas:

`git mergue xxxx-xxx`

Para actualizar la unión entre ramas:

`git mergue xxxx-xxx`

Traer un comit de alguna rama:

`git cherry-pick hash-de-la-rama-del-comit`

Rebase o traer los cambios del repo remoto al main repo en local:

`git pull -r origin main`
`git rebase --continue`

Crear un espacio para continuar en otro momento

`git stash`

Ver la lista de stashes

`git stash list`

Ver lo que contiene un slash

`git stash show`

## GitFlow Commands

Inicar gitflow: `git flow init`

Crear una feature:

`git flow feature start name-of-branch`

Publicar una feature:

`git flow feature publish name-of-branch`

Obtener una feature publicada

`git flow feature pull name-of-branch`

Finalizar una feature

`git flow feature finish  name-of-branch`

Crear una release

```bash
git flow release start v1.0.0
git tag -a v1.0.0 -m "Social auth feature"
git flow release publish social-auth
git push origin --tags
```

Preparar para subir los datos:

```bash
git add -A
git commit -m "social_auth_2.py fixed."
git push
git tag -a v1.0.2 -m "Social auth fixed."
git push origin --tags
Publicar la release
```

`git flow release publish v1.0.0`

Finalizar la release:

`git flow release finish v1.0.0`

Crear una Hotfixe:

`git flow hotfix start vx.x.x`

Creando el commit para el hotfix

```bash
git add -A
git commit -m "social_auth_2.py hotfix."
git push
git tag -a v1.0.3 -m "social auth hotfix."
git push origin --tags
```

Finalizando el hotfix

`git flow hotfix finish vv1.0.0`
