# Cómo hacer los ejercicios en KungFuPress Classroom

Estas pautas sirven para cualquiera de los ejercicios que te vaya proponiendo aunque voy a usar como ejemplo el tutorial ["Desarrollo de un formulario personalizado utilizando un plugin de creación propia"](https://kungfupress.com/como-programar-un-formulario-en-wordpress-sin-utilizar-plugins/). 

Si te resulta más cómodo tienes [estas mismas instrucciones en vídeo](https://youtu.be/dRuiJOhsVfM).

**Importante**: para hacer este ejercicio has debido recibir un enlace por correo electrónico. Si no es así envíame un correo a kungfupress@gmail.com solicitándolo e indicando cual es tu nombre de usuario en GitHub.

## Requisitos
Necesitas algunos requisitos antes de empezar a hacer este ejercicio:
* Instalación local de WordPress que esté funcionando donde vas a probar tu plugin.
* Instalar **Git** en local, tener una cuenta en GitHub y unas nociones básicas de Git.
* Entorno de desarrollo o editor de código en tu equipo. Te recomiendo **Visual Code Studio** por ser de código abierto, gratuito y ligero. Además ¡está de moda!

## Preparación del entorno de trabajo

Para realizar los tutoriales y poder ir comprobando lo que vas haciendo te hará falta colocar la carpeta del plugin (o del tema cuando toque) dentro de la carpeta **plugins** o **themes** de una instalación local de WordPress.

### WordPress local
La instalación de WordPress local la puedes instalar con cualquiera de estas soluciones, las pongo por orden de facilidad de instalación y uso:
* Utilizando [Local by Flywheel](https://localbyflywheel.com/).
* Cualquier aplicación tipo WAMP (windows), MAMP(mac),  LAMP(linux) o XAMPP (para los tres).
    * [Wamp Server](http://www.wampserver.com/en/).
    * [MAMP](https://www.mamp.info/en/)
    * [Instalar LAMP en Ubuntu 18.04](https://www.digitalocean.com/community/tutorials/como-instalar-en-ubuntu-18-04-la-pila-lamp-linux-apache-mysql-y-php-es).
    * [XAMPP - ApacheFriends](https://www.apachefriends.org/es/index.html).
* Utilizando Docker con un hub de WordPress
    * https://neliosoftware.com/es/blog/como-usar-docker-para-desarrollar-en-wordpress/
    * https://platzi.com/blog/wordpress-en-docker/
    * https://hub.docker.com/_/wordpress

### Git
Si  necesitas repasar tus conocimientos de Git te recomiendo el vídeo [Aprende Git en 30 minutos](https://www.youtube.com/watch?v=QGKTdL7GG24) (de momento bastaría con que controles hasta el minuto 15). En cuanto pueda quiero hacer uno más personalizado para el ecosistema WordPress. 
Si prefieres leer o quieres profundizar un poco más te recomiendo el libro [Aprende Git y de paso GitHub](https://github.com/JJ/aprende-git). 

Si utilizas Windows puedes descargar [Git para Windows](https://gitforwindows.org/), si usas Mac puedes instalar Git con [Homebrew](https://brew.sh/index_es )y si eres linuxero con tu gestor de paquetes favoritos aunque en la versiones actuales suele venir de serie. Si necesitas más información sobre la instalación te recomiendo el artículo ["Como instalar git en Windows, Mac y Linux"](https://filisantillan.com/como-instalar-git/)

### GitHub
Posiblemente ya tengas una cuenta en GitHub y puedes usar esa. Si no la tienes es un buen momento para [crear una](https://github.com/join?source=kungfupress). 

Si te vas a dedicar al desarrollo de código esta será una de las redes sociales donde más deberías trabajar tu perfil, así que elige un buen nombre de usuario que refleje tu marca personal. Procura que no lleve números a no ser que el número forme parte de la marca.

### Entorno de desarrollo
Si no estás habituado a ningún IDE (entorno de desarrollo), te recomiendo que empieces con [Visual Studio Code](https://code.visualstudio.com/). 

Una vez instalado puedes descargar algún plugin de este editor para WordPress, el más interesante es **WordPress VS Code Extension Pack**. Si da algún fallo durante la instalación o te pide instalar más cosas y no sabes seguir,  déjalo deshabilitado de momento, pero sigue con el ejercicio que es lo importante. Espero escribir un artículo sobre este tema en cuanto pueda.

## Accede al enlace del ejercicio recibido por correo
A continuación debes seguir el enlace del correo electrónico que has debido recibir para hacer el ejercicio. 

Cuando accedas al enlace, el sistema de **GitHub Classroom** va a crear dentro de **KungFuClass** un repositorio personalizado con tu alias de GitHub que es sobre el que tienes que trabajar para ir haciendo el ejercicio.

En ese repositorio ya tienes una plantilla inicial con cuatro ficheros:
* Fichero **.gitignore** preparado para WordPress, aunque casi no va hacer falta porque la raíz de este repositorio va a ser la propia carpeta del plugin.
* Fichero **LICENSE** con la licencia GPL que ampara a esta plugin para que sea software libre.
* Fichero **README.md** con unas sencillas instrucciones de lo que tienes que hacer para completar el ejercicio. Aunque tienes mayor detalle en el artículo del blog de KungFuPress.
* Fichero **kfc-form-autoevaluacion-tu-alias.php** que es el propio plugin y donde vas a trabajar prácticamente todo el tiempo. 

Cómo ves contiene un esqueleto muy básico para empezar a desarrollar el plugin.

Una vez echas las presentaciones, vas a copiar el repositorio a tu entorno de desarrollo y entonces ¡por fin! podrás empezar a escribir código en él.

Si todo esto te parece engorroso esta primera vez pronto te resultará algo natural, y no solamente tiene utilidad para hacer ejercicio de clase, sino que, he escogido precisamente este sistema, porque es el que utilizan actualmente todos los desarrolladores de código, ya trabajen en WordPress, JavaScript, PHP, Java, RubyOn Rails o lo que sea. Y esto es lo que deberías encontrar en cualquier entorno de trabajo serio, y si no, puedes aportarlo tú.

## Descarga del repositorio en local
Para copiar la URL del repositorio, ve a la página inicial del mismo, busca el botón verde **Clone or download** y copia la URL al portapapeles 📋

Ahora abres una terminal en tu equipo si estás en Mac o Linux, o desde una terminal especial para Git en Windows (también te hablé de ello en el correo) buscas el directorio donde tienes instalado tu WordPress local. 

Ve a la carpeta **wp-content/plugins**, ahí tecleas: ```git clone``` y pegas la URL del portapapeles. Pulsa ```enter``` para ejecutar el comando. 

Accede al directorio **kfc-form-autoevaluacion-tu-alias.php** que se acaba de crear.

Si tu shell está preparada para trabajar con repositorios de git es posible que el prompt cambie ligeramente de aspecto cuando estés dentro de un repositorio. Como ves dentro de este directorio están todos los archivos que estaban en GitHub.

## Accede al código desde el entorno de desarrollo
Ahora puedes empezar a trabajar desde Visual Studio Code, abres el programa y dentro abres la carpeta del plugin.

Para ver que todo está funcionando correctamente puedes modificar en la cabecera del plugin el campo **Author** con tu nombre.
Abres en tu navegador tu sitio WordPress local y accedes al panel de administración y en el menú de plugins verás el plugin **kfc-form-autoevaluacion-tu-alias** desactivado pero ahora debe aparecer tu nombre en él.

## Volviendo al terminal y a git
Por último, una vez que has comprobado que todo está preparado para empezar a trabajar debes actualizar el repositorio y subirlo a GitHub:
* Haz un ```git status``` para ver que hay un fichero que se ha modificado.
* Si llevaras un rato trabajando y no recordaras bien lo que has hecho puedes teclear ```git diff`` para que te muestre las líneas que han cambiado dentro del archivo. Sales de git diff pulsando la letra ```q```.
* Teclea ```git add .``` para agregar los cambios al **stage** de git.
* Agrega los cambios al repositorio local con ```git commit -m"Modifica el valor de author en la cabecera del plugin"```
* Con esto los cambios ya están recogidos en tu repositorio local, pero ahora debes hacer un ```git push``` para subir los cambios al repositorio remoto de GitHub, el que está en KungFuClass.
* Entra a la web de GitHub para ver que efectivamente los cambios se han subido.
* Sigue creando el plugin, haciendo commit, push a github y vuelta a empezar hasta terminar el tutorial. 

## Resumiendo
Esta sería la dinámica normal de trabajo: 
* Descargar el contenido del repositorio dentro de la carpeta **plugins** de una instalación local de WordPress.
* Ir haciendo los pasos del tutorial
* En cada uno de los apartados que voy marcando puedes hacer un commit y un push para que el trabajo quede recogido por etapas, de este modo podré ir viendo cada commit que hayas realizado para ver como has ido progresando, si te has equivocado en algún punto o si has introducido alguna mejora respecto del original.

El flujo sería igual en un entorno real de trabajo donde necesitaras implementar alguna mejora o nueva característica en el código e ir guardando los pasos a medida que las cosas vayan funcionando. También es recomendable al terminar una sesión de trabajo, donde en el mismo commit puedes dejarte un mensaje indicando que has hecho y donde lo dejas para continuar al día siguiente.

¿Has encontrado algún error? ¿Tienes una propuesta para mejorar esta guía? Si es así te agradezco infinito que [me dejes un issue](https://github.com/kungfuclass/como-hacer-los-ejercicios-en-kungfuclass/issues/new) para mejorarlo y así poder ayudar al resto de aprendices.
