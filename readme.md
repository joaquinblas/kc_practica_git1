# Práctica del curso de git, gitHub y Sourcetree

## ¿Qué comando utilizaste en el paso 11? ¿Por qué?

`git reset --hard HEAD~1` 

Uso HEAD~1 para ir un paso atrás y el --hard para perder los cambios.


## ¿Qué comando o comandos utilizaste en el paso 12? ¿Por qué?

`git reflog` y anoto el hash del commit que he deshecho anteriormente:

630b4ac HEAD@{1}: commit: añado cursivas a git-nuestro

`git reset --hard 630b4ac` 

Esto nos devuelve a situación en la que estábamos.


## El merge del paso 13, ¿Causó algún conflicto? ¿Por qué?
`git merge master`
➜  Already up-to-date.

No causa conflicto porque están en linea ambas ramas, styled contiene la info de master

## El merge del paso 19, ¿Causó algún conflicto? ¿Por qué?
Causa un conflicto porque el archivo git-nuestro.md tenía modificaciones en las mismas lineas del mismo documento en cada rama.


## El merge del paso 21, ¿Causó algún conflicto? ¿Por qué?
`git merge styled`
➜  Updating 75be8ba..c00a788
Fast-forward
 git-nuestro.md | 18 +++++++++---------
 1 file changed, 9 insertions(+), 9 deletions(-)

No hay conflictos porque al ser un merge Fast-forward la rama merge avanza a styled.

## ¿Qué comando o comandos utilizaste en el paso 25?

`git graph` 

Este es un alias de `git log --graph --decorate --pretty=oneline`


## El merge del paso 26, ¿Podría ser fast forward? ¿Por qué?
hacemos `git merge --no-ff title` y podría haber sido Fast-forward porque podríamos haber avanzado a title al estar en linea y title tener la información de master.


## ¿Qué comando o comandos utilizaste en el paso 27?
`git reset HEAD~1`
➜  Unstaged changes after reset:
M	git-nuestro.md

## ¿Qué comando o comandos utilizaste en el paso 28?
`git reset --hard HEAD~1`
➜  HEAD is now at 630b4ac añado cursivas a git-nuestro

## ¿Qué comando o comandos utilizaste en el paso 29?
`git branch -D title`
➜  Deleted branch title (was e35fb31).

## ¿Qué comando o comandos utilizaste en el paso 30?
`git reflog` y anoto el hash de hacer merge title en master:
70ceedd HEAD@{2}: merge title: Merge made by the 'recursive' strategy.

`git reset --hard  70ceedd` 
➜  HEAD is now at 70ceedd Merge branch 'title' 


## ¿Qué comando o comandos usaste en el paso 32?

Tenemos dos opciones:

`git log`
commit 75be8bae6c202f50a8a9b97f9c6a8c433b6cb0d5
Author: Joaquín Blas <joaquinblas@gmail.com>
Date:   Fri Jun 23 12:11:06 2017 +0200

    Creo git-nuestro

`git checkout 75be8bae6c202f50a8a9b97f9c6a8c433b6cb0d5` -> movería el puntero head

========

`git reflog`
75be8ba HEAD@{19}: commit (initial): Creo git-nuestro

`git reset --hard 75be8ba` -> volvemos al estado inicial cuando creamos el poema.

`git reset --hard 75be8ba`
➜  HEAD is now at 75be8ba Creo git-nuestro

## ¿Qué comando o comandos usaste en el punto 33?

`git reflog`
70ceedd HEAD@{4}: merge title: Merge made by the 'recursive' strategy.

`git reset --hard 70ceedd`
➜  HEAD is now at 70ceedd Merge branch 'title'


