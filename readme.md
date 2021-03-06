# **LABORATORIO 2 - PATTERNS - 2021-2**

## **LA HERRAMIENTA MAVEN**

+ Cuál es su mayor utilidad

	Maven se utiliza en la gestión y construcción de software. Posee la capacidad de realizar ciertas tareas claramente definidas, como la compilación del código y su empaquetado. Es decir, hace posible la creación de software con dependencias incluidas dentro de la estructura del JAR.
	
+ Ciclo de vida de la construcción

	Las partes del ciclo de vida principal del proyecto Maven son:
	
	1. **compile**: Genera los ficheros .class compilando los fuentes .java
	2. **test**: Ejecuta los test automáticos de JUnit existentes, abortando el proceso si alguno de ellos falla.
	3. **package**: Genera el fichero .jar con los .class compilados
	4. **install**: Copia el fichero .jar a un directorio de nuestro ordenador donde maven deja todos los .jar. De esta forma esos .jar pueden utilizarse en otros proyectos maven en el mismo ordenador.
	5. **deploy**: Copia el fichero .jar a un servidor remoto, poniéndolo disponible para cualquier proyecto maven con acceso a ese servidor remoto.

+ Para qué sirven los plugins

	En Maven, los plugins tienen metas, que según el técnico son solo métodos Java. Las metas ejecutan tareas de construcción como: compilar el proyecto, empaquetarlo e implementarlo en un servidor local o remoto. Esas actividades se correlacionan perfectamente para construir fases del ciclo de vida.

+ Qué es y para qué sirve el repositorio central de maven

	El repositorio central de Maven es la ubicación predeterminada para que Maven descargue todas las bibliotecas de dependencia del proyecto para su uso. Para cualquier biblioteca involucrada en el proyecto, Maven primero busca en la carpeta .m2 del Repositorio local, y si no encuentra la biblioteca necesaria, busca en el Repositorio central y carga la biblioteca en el repositorio local.

## **COMPILAR Y EJECUTAR**

+ Busque cuál es el objetivo del parámetro "package" y qué otros parámetros se podrían enviar al comando mvn.

	+ **mvn package**: Es el comando de empaquetado del proyecto maven. Para el proyecto java, ejecute el paquete y márquelo como un paquete jar, y para el proyecto web es un paquete war.
	
	+ **mvn compile**: Es el comando de compilación del proyecto maven, la función essrc/main/java Los archivos siguientes se compilan en archivos de clase y se envían al directorio de destino.
	
	+ **mvn test**: Es el comando de prueba mvn test del proyecto maven, que se ejecutarásrc/test/java AbajoClase de prueba unitaria.
	
	+ **mvn clean**: Es el comando de limpieza del proyecto maven. Ejecutar clean eliminará el directorio y el contenido de destino.
	
	+ **mvn install**: Es el comando de instalación del proyecto maven. La ejecución de install marcará maven en un paquete jar o paquete war y lo publicará en el almacén local.
	A partir de los resultados de la ejecución, se puede ver que cuando se ejecutan los siguientes comandos, las operaciones anteriores también se ejecutarán automáticamente.
	
	+ **mvn deploy**: Subir al almacén remoto
	
	+ Para mayor informacion ingresar a este [link](http://tutorials.jenkov.com/maven/maven-commands.html)
	
+ Busque cómo ejecutar desde línea de comandos, un proyecto maven y verifique la salida cuando se ejecuta con la clase App.java como parámetro en "mainClass".

	+ Para ejecutar desde la linea de comandos se va a utilizar el comando exec de la siguiente manera:
	
	```
	mvn exec:java -Dexec.mainClass="clase_principal_del_proyecto" -Dexec.args="argumentos_necesarios"
	```
## HACER EL ESQUELETO DE LA APLICACION

+ ¿Cuál(es) de las anteriores instrucciones se ejecutan y funcionan correctamente y por qué?

	+ De las 4 instrucciones anteriores se van a ejecutar correctamente todas pero solo una de ellas nos mostrara un resultado positivo que seria el caso de la instruccion con el parametro Hexagon.
	
	+ El porque de esto es devido a que al crear la clase tipo enum con los nombres de los objetos, solo se nos va a mostrar una correcta ejecucion con los parametros definidos en esta clase con la escritura exacta con la que se realizo, en cambio si se nos es enviado otro tipo de parametro la ejecucion simplemente nos mostrara un mensaje de error ya predefinido por nosotros.
	
## BIBLIOGRAFIA

+ <https://www.mojohaus.org/exec-maven-plugin/usage.html>
+ <https://programmerclick.com/article/81251978045/>
+ <http://tutorials.jenkov.com/maven/maven-commands.html>
+ <https://geekflare.com/es/apache-maven-for-beginners/>
+ <https://developer.ibm.com/es/articles/j-5things16/>
+ <https://es.wikipedia.org/wiki/Maven#Plugins_disponi>
+ <http://panamahitek.com/que-es-maven-y-para-que-se-utiliza/>