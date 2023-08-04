# Practica con Git Colaborativo
## Glosario

- *Rama (branch)*. Es una 'version' del proyecto. Existe una rama principal que es el origen de todas las ramas y se pueden ir creando más a partir de esta, la utilidad es separar funcionalidades o versiones. En ocasiones una rama se puede fusionar con otra. 
- *Clonar (clone)*. Hacer una copia local de un proyecto junto con todas sus ramas
- *Jalar (pull)*. Es actualizar la copia local con los nuevos cambios que puedan existir en la versión remota. 
- *Añadir (add)*. Cuando modificamos nuestra versión local y queremos subir nuestro código podemos añadir (add) nuestros archivos para un posible commit.
- *Confirmar (commit)*. Confirma todo nuestro (add), la idea es incluir un mensaje para que se sepa que cambios trae esta nueva versión que se piensa subir a la rama
- *Empujar (push)*. Publicar nuestros cambios en la versión remota

## Ejercicios

1. Clonar el repositorio, puedes utilizar la técnica de clonación por medio de una llave SSH [Github SSH Key Tutorial](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent#generating-a-new-ssh-key)

    - *Clonar un repositorio es copiar un proyecto junto con todas sus ramas* <br/><br/>

    - Ubicarse con una terminal en el siguiente donde viven las llaves SSH
        - Windows: `C:\Users\<NOMBRE_DEL_USUARIO>\.ssh`
        - Linux: `~/.ssh/`
        - MacOS: `~/.ssh/`
    - Crear llave ssh como en el tutorial de Github SSH Key Tutorial, con el comando `ssh-keygen`
    - Recordar la contraseña para utilizarla después<br/><br/>
    - Ubicarse en el directorio donde queramos clonar el repo
    - Intentar clonar el repo con el siguiente comando
        - `git clone git@github.com:mx-labo/git-colaborativo.git`

2. Hacer un pull, para probar nuestra llave SSH 
    - `git clone git@github.com:mx-labo/git-colaborativo.git`
    - Introducimos nuestro pwd
    - Debemos visualizar en nuestra terminal la nueva actualización o si ya tenemos la última actualización solo debemos ver un mensaje que todo esta actualizado

3. Hacer un push, probar el poder subir cambios
    - Crear un archivo, por ejemplo <USUARIO_GITHUB>.txt
    - Introducir algo dentro de ese archivo, por ejemplo "Mis cambios para master"
    - Guardar archivo
    - Dentro de la terminal, hacer un add del nuevo archivo:
        - `git add <USUARIO_GITUB>.txt`
    - Después hacer el commit:
        - `git commit -m "Subiendo mi archivo a master de prueba"` La bandera `-m` permite hacer un commit inmediato donde estas haciendo el commit y al mismo tiempo poniendo el mensaje referente a ese commit 
    - Intentar hacer el push:
        - `git push origin -u master` La bandera `-u` indica que la rama con la que estamos trabajando y queremos publicar
    - Si todo es correcto la consola nos debe arrojar que se ha publicado el nuevo commit, de lo contrario quizá debamos primero hacer un `git pull` porque puede que haya una versión más nueva remota

