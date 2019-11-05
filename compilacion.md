### Contenido de del directorio de compilación de less

- Ficheros fuente con extensión .c
- Ficheros objeto con extensión .o. Se compilan individualmente en ficheros objetos con extensión .ko.
- Ficheros con extensión .h, cabeceras (header), parte de la anatomía del lenguaje C.

### Para configurar el paquete para mi sistema
~~~
$ ./configure 
~~~

> Ejemplo falta una librería:
El comando anterior no se ha terminado correctamente porque falta una libreria, en este caso aparece el siguiente mensaje:
~~~
checking for working terminal libraries... Cannot find terminal libraries - configure failed
~~~

Se necesita la siguiente librería
~~~
$ sudo apt install libtinfo-dev
~~~

### Compilar
~~~
paloma@coatlicue:~/DISCO2/less$ make
~~~

### Instalación:
~~~
paloma@coatlicue:~/DISCO2/less$ sudo make install
~~~

# OPCIONES DE INSTALL PARA ENTENDER LA INSTALACIÓN CON MAKE

-**c** No hace nada; por compatibilidad con viejas  versiones  de install  de  Unix,  donde  significaba  "copiar" en vez de
              "mover". Esta versión siempre copia.
-**m modo, --mode=modo** Establece el modo de permisos para el fichero instalado  o directorio a modo, que puede ser un número octal o un modo simbólico como en chmod, siendo 0 el punto de partida.  El modo   predeterminado   es   0755:  lectura,  escritura  y ejecución para el propietario, y lectura y ejecución  para el grupo y para los otros.


### Desinstalación manual
En el fichero INSTALL se indica lo siguiente:
> By default, `make install' will install the package's files in
`/usr/local/bin', `/usr/local/man', etc.  You can specify an
installation prefix other than `/usr/local' by giving `configure' the
option `--prefix=PATH'.

Esto significa que los ficheros al instalarse se encuentran en estas dos direcciones.



### Opciones de make
**make clean** Elimina los archivos binarios del programa y los archivos de objetos del directorio fuente que se han creado durante la compilación.
 

**make distclean** Como clean pero también borra los ficheros de configuración.

**make install** 
**make uninstall**

**make configure** Para configurar la compilación:
- **config.status** Fichero para poder recrear la configuración actual.
- **config.cache** Fichero para guardar los resultados de sus pruebas.
- **config.log** Fichero que contiene la salida del compilador.



