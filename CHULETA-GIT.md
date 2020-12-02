# Chuleta GIT

## Obtener cambios en Github
`git fetch` 
Trae información de ramas nuevas y cambios pero no los aplica.

## Trabajar con ramas sincronizadas con main

### Hacer un branch desde main/master
`git checkout main`
`git pull` Actualizar Rama
`git checkout -b nuevaRama`

## Borrar Ramas
### Rama local
Ramas con todos los cambios confirmados
`git branch -d nombre rama`
Si tienes cambios pendientes
`git branch -D nombre rama`
### Rama Remota
`git push origin --delete nombrerama`
## Deshacer cambios
### Revertir cambios públicos con Revert
`git revert -n -m 1 hashinicial..HEAD`
Es un proceso de varios pasos que requiere solucionar conflictos y avanzar hasta llegar al final del proceso con el comando
`git revert --continue`
[Referencia StackOverflow](https://stackoverflow.com/questions/4114095/how-do-i-revert-a-git-repository-to-a-previous-commit)
[Revert Man page](http://schacon.github.io/git/git-revert.html)
### Revertir cambios públicos exportando, limpiando y sobrescribiendo
1. Exportar archivo
2. `git archive -o inicial.zip 879b84c`
3. Eliminar todos los archivos de forma manual excepto el directorio **.git** y el **.zip**
4. Descomprimir el archivo **.zip** creado
5. Seguir el ciclo de git add, commit, etc.

[Referencia git-scm](https://git-scm.com/docs/git-archive)
[Referencia StackOverflow](https://stackoverflow.com/questions/160608/do-a-git-export-like-svn-export)

