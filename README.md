# GIT ramas (Branches)

## Crear un repositorio 

```sh
git init
```

## Ver el estado de los archivos

```sh
git status
```

## GIT Alias

```sh
git config --global alias.st "status --short"
git config --global alias.a "add"
git config --global alias.c "commit -m"
git config --global alias.l "log --oneline"
```

## Ver las diferencias entre el WD y LR 

```sh
git diff
```

## Ver el contenido de cada commit

```sh
git show <número-hash>
```

## Crear una rama 

```sh
git branch <nombre-rama> # crea una rama y nos deja en la rama original
git branch feature/ramas # ejemplo
git switch -c <nombre-rama> # Crea una rama y nos mueve a la rama que se creó
```

## Me mueve entre ramas

```sh
git switch <nombre-rama>
git switch feature/ramas # ejemplo
```

## Ver las ramas locales y remotas

```sh
git branch -a # Me muestra las ramas locales y remotas
```

## Fusionando ramas
Estoy sobre la rama main y me quiero traer lo que está en feature/ramas

```sh
git merge <rama-que-quiero-fusionar>
# ejemplo
git switch main 
git merge feature/ramas # me traigo a main lo que tenía en feature/ramas
```

* fusión -> fast-forward -> git hace la fusión automáticamente.

## Eliminar una rama 

```sh
git branch -d <nombre-rama> # Si la rama que estoy borrando ya fue fusionada se va a borrar la rama.
git branch -D <nombre-rama> # Confirmación de borrado de una rama que todavía no ha sido fusionada en el repositorio.
git branch -d feature/ramas # Ya estaba fusionada feature/ramas
git branch -D alejo # No estaba fusionada por lo cual me pidió confirmación.
```

## Abortar la fusión

```sh
git merge --abort
```