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

Envía cambios al repostiorio con un mensaje indicativo sobre los cambios realizados (para salir esc-shift-z-z)

`git commit`

Como no le enviamos un mensaje, abre el editor de código basado en la linea de comandos(vim), solicitando el mensaje referente a los cambios. Luego envía los cambios al repositorio. (EL control de versiones no permite cambios vacíos)

`git rm --cached archivo.txt`

Devuelve el archivo a su estado anterior

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

`git diff version1 version2`

Podemos comparar los cambios entre diferentes versiones del archivo






