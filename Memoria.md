# 1) Conexión

Primero se hace la conexión entre la máquina virtual y nuestro IDE, en este caso Visual Studio Code, a través de SSH con la extensión de VSCode Remote-SSH. Utilizamos la IP dinámica que te salga al utilizar el comando `ip a`.

# 2) Creación de zona de trabajo

Creamos la carpeta en la que vamos a realizar la práctica y en ella creamos el archivo de configuración `docker-compose.yml`, el fichero `.env` y el archivo `.md`. Desde el archivo de Docker inicializamos los contenedores y trabajamos con ellos.

# 3) Subir archivos a GitHub

Como Ubuntu Server ya viene con Git instalado de serie, simplemente hay que inicializar el repositorio con `git init`, y seguir con los comandos:

`bash`
git add .
git commit -m "mensaje"
git branch -M main
git remote add origin https://github.com/SamuRebollo15/practicaDocker.git
git push -u origin main

# 4) Comprobar el funcionamiento de nuestros contenedores

Después de crear los contenedores, comprobamos que todo esté funcionando correctamente con el comando `docker ps`, que nos mostrará los contenedores y los volúmenes asociados. 

Luego, abrimos un navegador y accedemos utilizando la IP de nuestra máquina junto con el puerto asignado para el contenido de los contenedores. Por ejemplo, en mi caso, al ingresar `10.6.9.60:8081`, aparecía la pantalla de phpMyAdmin, lo que confirmaba que los contenedores y su configuración estaban correctamente implementados.
