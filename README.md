# Terminal - Comandos básicos
ver contenido - ls <br>
desplazarse - cd <directorio><br>
volver atrás - cd ..<br>
saber ruta actual - pwd<br>
crear carpeta - mkdir <nombre><br>
crear archvio vacío en el directorio actual - touch <nombre><br>
eliminar archivo/carpeta - rm <nombre><br>
copiar un archivo de un lugar a otro - cp <nombre> <directorio><br>
mover un archivo de un sitio a otro - mv <nombre> <directorio><br>



# ver versión
git --version <br>
git -v

# ayuda
git -h

# Configuración
Todas las acciones que realizamos deben estar asociadas a un autor. Es una forma fácil de saber quién hizo un cambio en el programa. De este modo, si hay algún problema podemos saber quién fue y quién y cuándo se causó el problema.

Ayuda - git config
configurar nombre - git config --global user.name <nombre><br>
configurar email - git config --global user.email <email><br>

podemos poner un alias a un comando que usemos mucho para facilitarnos el trabajo
git config --global alias.<nombre> "log --graph --decorate --all --oneline"

# Inicialización de un repositorio

## Por qué se debe iniciar?
Si no se inicia, git no sabe si se ha creado un repositorio
inicializar un repositorio - git init

Al ejecutar el comando anterior, git creará una carpeta oculta llamada .git. Esta carpeta contiene todas las referencias asociadas al sistema de control de versiones y es obligatorio antes de poder realizar cualquier otra acción propias de git.

## Qué es un repositorio?
Es el lugar donde se guardan todos los cambios realizados en el proyecto. Desde la fecha de los cambios, diferentes versiones, documentación y cualquier otra cosa que se encuentre en el repositorio. Cada versión de un archivo se asocia a un commit.
Los repositoriores pueden ser: <br>
Locales: se almacenan en nuestro equipo<br>
Remotos: se almacenan en un servidor en la nube

# Ramas
Git se inicia siempre con una rama princial "master" pero podemos cambiarla por otro nombre (normalmente a "main", "trunk" o "development")
git branch -m <nombre>

Si queremos que la rama principal siempre se llame iguale cada vez que creemos un repositorio podemos usar el siguiente comando
git config --global init.defaultBranch <nombre>

# Guardar estado actual
para ver el estado actual<br>
git status - Nos saldrá en rojo los cambios que no hayamos añadido, y en verde los que sí

```
$ git status
On branch main

No commits yet

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        hello_git.txt (en ROJO)
        hellogit.py (en ROJO)

nothing added to commit but untracked files present (use "git add" to track)
```

Para añadir un fichero a git
git add <nombre_fichero>

Si se vuelve a hacer git status los ficheros que hayamos añadido ahora nos saldrán en verde

para añadir todos los ficheros
git add .

actualizar repositorio (Obligatorio poner un comentario)
git commit -m "mensaje"

# Ver historial de commits
git log
git log --graph
git log --graph --pretty=oneline
git log --graph --decorate --all -oneline


# El comando checkout nos permite situarnos en un punto concreto del historial de commits o de un archivo
git checkout <nombre_fichero>

# si queremos volver al último commit completo creado
git reset







