## Comandos git

`git init`

Inicializa un archivo .git en nuestro repositorio, donde estará la base de datos de los cambios

`code .`

Abre el editor de código (Ejemplo, VSC)

`git status`

Muestra el estado de los archivos en el proyecto. En que rama se encuentran, y si ya han pasado por "commit"

`git add archivo.txt`

Cambia el estado del archivo al "stage"

`git add .`

Cambia el estado del todos los archivos del repositorio al "staging area" de la memoria RAM

`git commit -m "mensaje de la modificación"`

Envía cambios al repostiorio con un mensaje indicativo sobre los cambios realizados

`git commit`

Como no le enviamos un mensaje, abre el editor de código basado en la linea de comandos(vim), solicitando el mensaje referente a los cambios. Luego envía los cambios al repositorio. (El control de versiones no permite cambios vacíos)
(para salir shift-z-z)

`git rm`

Este comando nos ayuda a eliminar archivos de Git sin eliminar su historial del sistema de versiones. Esto quiere decir que si necesitamos recuperar el archivo solo debemos “viajar en el tiempo” y recuperar el último commit antes de borrar el archivo en cuestión

`git rm --cached archivo.txt`

Elimina los archivos de nuestro repositorio local y del área de staging, pero los mantiene en nuestro disco duro. Básicamente le dice a Git que deje de trackear el historial de cambios de estos archivos, por lo que pasaran a un estado untracked.

`git rm --force archivo.txt`

Elimina los archivos de Git y del disco duro. Git siempre guarda todo, por lo que podemos acceder al registro de la existencia de los archivos, de modo que podremos recuperarlos si es necesario (pero debemos usar comandos más avanzados)

`git config --list`

Muestra la lista de configuraciones por defecto que contiene nuestro git

`git config --list --show`

Muestra donde están guardadas las configuraciones

`git config --global user.name "tu nombre"`

Modifica la configuración global del nombre

`git config --global user.email "tu email"`

Modifica la configuración global del email

`cat archivo.txt`

Nos permite ver el archivo por dentro

`git show archivo.txt`

Muestra todos los cambios realizados en el archivo

`git log archivo.txt"`

Nos permite ver los commits realizados en el archivo, con autor y fecha

`git log --stat`

Nos permite ver los commits realizados con más profundidad

`git diff version1 version2`

Podemos comparar los cambios entre diferentes versiones del archivo

`git reset version2 --hard`

Borra todo. Todo todito, absolutamente todo. Toda la información de los commits y del área de staging se borra del historial.

`git reset version2 --soft`

Borramos todo el historial y los registros de Git pero guardamos los cambios que tengamos en Staging, así podemos aplicar las últimas actualizaciones a un nuevo commit.

`git reset HEAD version2 `

Este es el comando para sacar archivos del área de staging. No para borrarlos, solo para que los últimos cambios de estos archivos no se envíen al último commit, a menos que cambiemos de opinión y los incluyamos de nuevo en staging con `git add`

`git clone url`

Traer un repositorio de github a nuestro repositorio local y a nuestro directorio de trabajo

`git push origin (rama)`

Enviar todos los cambios al repositorio remoto (origin es un nombre opcional pero se usa por convención)

`git fetch`

Trae al repositorio local los cambios realizados por otros desarrolladores. Luego debemos hacer `git merge` para traerlo a nuestro directorio de trabajo

`git pull origin (rama)`

Realiza la tarea de `git fetch` y `git merge` al mismo tiempo. Trae todo el repositorio remoto a nuestro repositorio local y los fusiona

`git pull origin (rama) --allow-unrelated-histories`

Fusiona el repositorio local con el remoto de manera forzosa

`touch index.html`

Touch crea un nuevo archivo en la carpeta en la que estamos ubicados

`git commit -am`

Realiza la tarea de `git add .` y `git commit -m` al mismo tiempo (solo si el archivo ya tuvo al menos un `git add .`)

`git branch nueva_rama`

Abre una nueva rama en el proyecto

`git show-branch`

Nos muestra el hisotiral de ramas del proyecto

`git show-branch --all`

Nos muestra el hisotiral de ramas del proyecto con información más detallada

`git checkout archivo.txt`

Nos devuelve a la versión del archivo que le indicamos

`git checkout nueva_rama"`

Nos coloca sobre la nueva rama. También poedemos volver a master, es decir, nos permite movernos entre rama y rama, y realizar cambos sin que una afecte a la otra

`git log --graph`

Luego de hacer un merge. con ese comando podemos ver en detalle el proceso de fusión de ambas ramas

`git log --graph --decorate --oneline`

Podemos ver todo la evolución del proyecto de forma más comprimida

`git remote add origin (ruta)`

Sincronizamos el repositorio a la ruta de github para subirlo

`git remote -v`

Podemos ver la ruta de fecth

`ssh-keygen -t rsa -b 4096 -C "youremail@example.com"`

Generar una nueva llave SSH (Con cualquier sistema operativo). Es aconsejable estar parado sobre ~

`cat id_rsa.pub`

Si estás parado sobre tu archivo .ssh (`cd ~/.ssh/`), con este comando puedes acceder al contenido de tu llave pública

`cat id_rsa`

Si estás parado sobre tu archivo .ssh (`cd ~/.ssh/`), con este comando puedes acceder al contenido de tu llave privada. IMPORTANTE: NUNCA SE LA MUESTRES A NADIE

`git remote set-url origin (url)`

Cambiar la ruta de nuestra url al repositorio remoto en github

`alias nombreCreado="comando"`

Nos permite crear un alias para nombrar a ese comando en adelante cada vez que lo queremos ejecutar

`git tag -a nombreEscogido -m`

Nos permite crear etiquetas que luego quedarán almacenadas y organizadas en Github

`git tag`

Podemos visualizar los tags activos en nuestro proyecto

`git tag -d nombreEscogido`

Borrar el tag en git

`git push origin --tags`

Empuja los tags al repositorio de Github

`git push origin :refs/tags/nombreEscogido`

Borrar el tag en Github

