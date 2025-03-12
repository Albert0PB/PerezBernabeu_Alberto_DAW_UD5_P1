# Ejercicios de Git y GitHub

## Ejercicios de Git y GitHub (I)

### Creación del repositorio y primer commit 

Para la realización de esta práctica se ha creado un 
repositorio remoto en GitHub:

![Repositorio remoto](./images/repositorioremoto.png)

También es necesario inicializar un repositorio en local, 
indicando la URL (en mi caso uso el enlace SSH) del 
repositorio remoto como "origen" y renombrando la rama 
"master" a "main":

![Inicialización repo local](./images/repositoriolocal.png)

A continuación, se realizará un primer commit sencillo 
en el que se subirá un archivo 'README.md' a la rama 'main' 
del  repositorio remoto:

![Primer commit](./images/primercommit.png)

### Ignorar archivos

En ocasiones tendremos en nuestro repositorio local archivos y/o
directorios que no queremos añadir a un commit (por ejemplo, 
archivos que guarden variables de entorno). Para mostrar cómo 
ignorar archivos, se crearán un archivo y un directorio de 
ejemplo:

![Archivo y directorio privados](./images/privados.png)

Y para ignorarlos (por ejemplo si ejecutásemos 'git add .'), 
creamos un archivo '.gitignore' con el siguiente contenido:

```git
privada
privada/*
privado.txt
```

### Tags

Crearemos un nuevo archivo '1.txt' y asignaremos un tag 
al commit antes de subir los cambios al repositorio remoto:

![Git tag](./images/gittag.png)

### Cuenta de GitHub

GitHub permite personalizar el perfil de la cuenta (Settings > Public profile). 
Por ejemplo, podemos poner una foto de perfil:

![Foto de perfil](./images/fotoperfil.png)

También es posible mejorar la seguridad de la cuenta activando la autenticación 
de dos factores (en mi caso, tengo activada la 2FA con la aplicación de autenticación 
de Google):

![Autenticación dos factores](./images/2fa.png)

### Uso social de GitHub

A través de GitHub podemos visitar las cuentas de otras personas. Voy a seguir 
a dos de mis compañeros de clase:

![Primer compañero](./images/compañero1.png)

![Segundo compañero](./images/compañero2.png)

También crearé una tabla con información de algunos de mis compañeros en el 
fichero README.md del repositorio DEAW:

![Tabla](./images/tabla.png)

### Gestión de rama v0.2

#### Creación de la rama

Creamos una rama con nombre 'v0.2', nos posicionamos sobre ella, creamos un 
fichero y subimos los cambios al repositorio remoto:

![Creación rama v0.2](./images/ramav02.png)

#### Merge directo

Podemos fusionar el contenido de la rama 'main' con el contenido de 'v0.2'. Como 
los archivos que comparten las dos ramas tienen el mismo contenido, simplemente se 
añadirá el archivo '2.txt' de 'v0.2' a 'main':

![Merge directo](./images/mergedirecto.png)

#### Merge conflictivo

Si quisiéramos realizar una fusión de ramas pero alguno de los archivos tuviera 
diferente contenido en cada rama, tendríamos que resolver el conflicto para que 
la fusión pueda realizarse. Por ejemplo, escribiré "Hola" en el '1.txt' de 'main' 
y "Adiós" en el mismo archivo pero en la rama 'v0.2':

![Diferente contenido en archivo](./images/diferentecontenido.png)

Al intentar fusionar las ramas saltará un aviso debido al conflicto en el 
contenido del archivo en las diferentes ramas:

![Aviso resolver conflicto](./images/avisoconflicto.png)

Si abrimos el archivo con un editor de texto se nos mostrará el contenido de 
ambas ramas:

![Editando contenido conflictivo](./images/editandocontenido.png)

Resolvemos el conflicto de contenido y confirmamos los cambios con un 'commit'.

#### Borrar rama

Creamos un tag 'v0.2' y borramos la rama con el mismo nombre:

![Borrar rama](./images/borrarrama.png)

#### Listar cambios

Para ver el historial de cambios utilizamos 'git log':

![Historial de cambios](./images/listarcambios.png)

## Ejercicios de Git y GitHub (II)

### Creación y actualización de repositorios

#### Ejercicio 1

Para definir el nombre de usuario, email y activar el coloreado de salida 
ejecutamos:

![Configurar Git](./images/configurargit.png)

Para mostrar la configuración ejecutamos:

![Mostrar configuración](./images/mostrarconfiguracion.png)

#### Ejercicio 2

Creamos un nuevo repositorio y mostramos su contenido:

![Nuevo repositorio](./images/repolibro.png)

#### Ejercicio 3

Comprobamos el estado del repositorio, creamos un fichero 'indice.txt' 
y comprobamos de nuevo el estado del repositorio:

![Primer estado](./images/primerestado.png)

Añadimos el fichero a la zona de 'stage' y volvemos a comprobar 
el estado del repositorio:

![Segundo estado](./images/segundoestado.png)

#### Ejercicio 4

Confirmamos los cambios y volvemos a comprobar el estado del repositorio:

![Tercer estado](./images/tercerestado.png)

#### Ejercicio 5

Modificamos 'indice.txt', mostramos los cambios con respecto a los cambios 
confirmados anteriormente y confirmamos la nueva versión del archivo:

![Modificación del índice](./images/modificarindice.png)

#### Ejercicio 6

Ahora mostraremos los cambios sobre la última versión del repositorio al 
completo. Después modificamos el mensaje de la última confirmación y 
veremos la última modificación realizada en el repositorio:

![Modificación del repositorio](./images/modificarrepositorio.png)

### Manejo del historial de cambios

#### Ejercicio 1

Mostramos el historial de cambios:

![Historial de cambios](./images/historialdecambios.png)

Añadimos un nuevo directorio y archivo, movemos el nuevo contenido a la 
zona de 'stage' y confirmamos los cambios:

![Capítulo 1](./images/capitulouno.png)

Volvemos a mostrar el historial de cambios:

![Historial de cambios 2](./images/historialdecambios2.png)

#### Ejercicio 2

Añadimos un nuevo capítulo y mostramos las diferencias entre la 
última versión y dos versiones anteriores:

![Historial de cambios ej2](./images/histej2.png)

#### Ejercicio 3

Añadimos un nuevo capítulo y mostramos las diferencias entre la 
primera y última versión del repositorio:

![Historial de cambios ej3](./images/histej3.png)

#### Ejercicio 4

Modificamos el archivo 'indice.txt', confirmamos los cambios y 
mostramos quién ha realizado los cambios sobre el fichero:

![Historial de cambios ej4](./images/histej4.png)

### Deshacer cambios

#### Ejercicio 1

Modificamos 'indice.txt' eliminando contenido y comprobamos el 
estado del repositorio. Después deshacemos los cambios y volvemos 
a comprobar el estado del repositorio:

![Deshacer cambios ej1](./images/deshej1.png)

#### Ejercicio 2

Volvemos a modificar 'indice.txt', añadimos los cambios a la zona 
de 'stage' y comprobamos el estado del repositorio. Después quitaremos 
los cambios de la zona de 'stage' y volvemos a comprobar el estado del 
repositorio. Por último, deshacemos los cambios y comprobamos el estado 
del repositorio:

![Deshacer cambios ej2](./images/deshej2.png)

#### Ejercicio 3

En primer lugar:

- Eliminamos la última línea del fichero indice.txt y guardarlo.
- Eliminamos el fichero capitulos/capitulo3.txt.
- Añadir un fichero nuevo capitulos/capitulo4.txt vacío.
- Añadir los cambios a la zona de intercambio temporal.

Tras los cambios, comprobamos el estado del repositorio. Después quitaremos 
los cambios de la zona de 'stage' y comprobamos el estado. Por último, 
deshacemos todos los cambios y comprobamos el estado por última vez:

![Deshacer cambios ej3](./images/deshej3.png)

#### Ejercicio 4

En primer lugar:

- Eliminar la última línea del fichero indice.txt y guardarlo.
- Eliminar el fichero capitulos/capitulo3.txt.
- Añadir los cambios a la zona de intercambio temporal y hacer un commit con el mensaje “Borrado accidental.”
- Comprobar el historial del repositorio.
- Deshacer el último commit pero mantener los cambios anteriores en el directorio de trabajo y la zona de intercambio temporal.

![Deshacer cambios ej4.1](./images/deshej4-1.png)

En segundo lugar:

- Comprobar el historial y el estado del repositorio.
- Volver a hacer el commit con el mismo mensaje de antes.
- Deshacer el último commit y los cambios anteriores del directorio de trabajo volviendo a la versión anterior del repositorio.
- Comprobar de nuevo el historial y el estado del repositorio.

![Deshacer cambios ej4.2](./images/deshej4-2.png)

### Gestión de ramas

#### Ejercicio 1

Creamos una nueva rama y mostramos todas las ramas del repositorio:

![Gestión de ramas ej1](./images/gestej1.png)

#### Ejercicio 2

Creamos 'capitulos/capitulo4.txt', confirmamos los cambios y 
mostramos el historial de todas las ramas:

![Gestión de ramas ej2](./images/gestej2.png)

#### Ejercicio 3

Nos movemos a la rama 'bibliografia', creamos un archivo de texto 
con el miso nombre y confirmamos los cambios, luego mostramos el 
historial con todas las ramas:

![Gestión de ramas ej3](./images/gestej3.png)

#### Ejercicio 4

Fusionamos 'bibliografia' con 'main', mostramos el historial, 
eliminamos 'bibliografia' y volvemos a mostrar el historial:

![Gestión de ramas ej4](./images/gestej4.png)

#### Ejercicio 5

Creamos una nueva rama 'bibliografia', modificamos 'bibliografia.txt' y 
confirmamos los cambios. Modificamos el mismo archivo en la rama 'main', 
los confirmamos y fusionamos las ramas resolviendo el conflicto en el 
fichero:

![Gestión de ramas ej5](./images/gestej5.png)

Mostramos el historial del repositorio:

![Gestión de ramas ej5 historial](./images/gestej5-hist.png)

### Repositorios remotos

#### Ejercicio 1

Creamos un nuevo repositorio en GitHub 'libro-git':

![Repositorio libro-git](./images/repremej1-1.png)

Lo añadimos al repositorio local y mostramos los repositorios remotos:

![Añadir el repositorio remoto al local](./images/repremej1-2.png)

#### Ejercicio 2

Subimos los cambios al repositorio remoto con:

```console
git push origin main
```

Comprobamos el historial de versiones del repositorio remoto:

![Repositorios remotos ej2](./images/repremej2.png)
