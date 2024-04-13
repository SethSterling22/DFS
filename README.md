# DFS
Distributed File System
# Número de estudiante: 801-21-1038 
# Clase: Operating Systems CCOM4017
# Profesor: José R. Ortiz Ubarri


# Descripción de los programas:

El documento presente consta de una serie de archivos, los cuales son: copy.py, createdb.py, 
data-node.py, dfs.db, ls.py, mds_db.py, meta-data.py, Packet.py y
los archivos de test que son test1.py y testdb.py; cada uno de los archivos 
hace parte del "Distrinuted File System" en mayor y menor medida.

# Cómo utilizar los programas:


● createdb.py:

Para ejecutar este programa se debe utilizar el siguiente comando:

○ python createdb.py

Al realizar esta acción, se crea la base de datos que se estará utilizando en el resto del
sistema de archivos distribuidos.

○ Su funcionamiendo es el de almacenar la información de los archivos tanto como su tamaño como su nombre/directorio
para de esta manera poder recuperarlos y ejecutar las acciones que el meta-data.py (que es quien tiene conexión) solicite.



● mds.db:

○ Su funcionamiento es servir de librería para la base de datos y el data-node para crear, empaquetar y recuperar la información
de los archivos almacenados en la base de datos.



● meta-data.py:

Para ejecutar este programa se debe utilizar el siguiente comando:

○ python meta-data.py

Al realizar esta acción, se crea el servidor localhost en el puerto 8000 (por defecto)

○ Su funcionamiento es quedarse pendiente a cualquier acción/comando que se envíe para 
sucesivamente realizar la conexión a la base de datos donde se encuentra toda la información de 
los archivos y en base a esa información y comandos, realizar sus diferentes funciones.




● data-node.py:

Para ejecutar este programa se debe utilizar el siguiente comando:

○ python data-node.py <server> <port> <data path> <metadata port,default=8000>

Al realizar esta acción, se crea el nodo de datos conectado al "meta-data server"

○ Su funcionamiento guardar la información fragmentada de los archivos para manejarla de manera más
eficaz y optimizada.




● ls.py:

Para ejecutar este programa se debe utilizar el siguiente comando:

○ python ls.py <server> <port>

Al realizar esta acción, se manda el request al "meta-data server" para mostrar todos los archivos
existentes en la base de datos.

○ Su funcionamiento es conectarse al "meta-data server" y enviar el comando de list para que se ejecute
la función "handle_list" la cual se conecta a la base de datos y recupera los nombres y el tamaño de todos
los archivos almacenados en la base de datos y los imprime para que el usuario pueda verlos.




● copy.py:

Para ejecutar este programa se debe utilizan los siguientes comandos dependiendo de qué acción se quiera realizar:

○ Copiar desde el DFS: python copy.py <server>:<port>:<dfs file path> <destination file>

Al realizar esta acción, se recopia la información de los data-nodes del archivo que estás solicitando y se copian
al directorio que se pasó.


○ Copiar hacia el DFS: python %s <source file> <server>:<port>:<dfs file path>

Al realizar esta acción, se busca en el directorio que le pasaste, el archivo y realiza una fragmentación del mismo
por la cantidad de data-nodes conectados y los manda a cada uno.

○ Su funcionamiento es tanto enviar la información de los archivos desde tu dispositivo local hacia el servidor
como al revés, de esta manera realizando de copiar un archivo o directorio de una dirección a otra.



● Packet.py:

○ Su funcionamiento es la de servir como librería de donde los demás programas van a tomar sus funciones.


● test1.py y testdb.py

Al ejecutarlos, cumplen la labor de probar las funciones básicas del funcionamiento del "meta-data server" y de la base de datos


# Referencias adicionales y colaboradores

//Se utilizó la refencia de video tal como:

● DFS illustrated
○ https://youtu.be/xBVMHMxZcAA

//También se utilizó material visto en la clase y presentado en las diapositivas.
 
//Se permitieron colaboraciones verbales, sin embargo, no se permitió el intercambio de 
código entre los colaboradores.

//Colaboradores:
   - Adriana Hernández Vega
