# automation_postman_pet_shop ![Status badge](https://img.shields.io/badge/status%20-finished-green)

* Este proyecto nos permite automatizar los servicios de la pagina de petstore de una forma dinamica, se reutiliza el código lo más que se pueda, se realiza el testeo de la respuesta que nos manda el end point, se verifica el status, la información que nos envía como respuesta,el esquema del json y tiempo que tarda cada end point.

## 🚀 Comenzando :

* Estas instrucciones te permitirán obtener una copia del proyecto en funcionamiento en tu máquina local para propósitos de desarrollo y pruebas.


## 📋 Pre-requisitos :

1. Clonar este proyecto.
2. Tener instalado postman en tu maquina.
3. Tener instalado newman y newman-reporter-htmlextra para poder generar el reporte.

Nota : Para instalar newman abrimos un cmd e ingresamos la siguiente linea de código:  npm install -g newman
       Para instalar newman-reporter-htmlextra en el mismo cmd ingresamos la siguiente linea de código: npm install -g newman-reporter-htmlextra

4.  Importar en postman el archivo de collection y enviroment.

Nota : Para importar en postman, hacemos clic en el menú file -> import -> upload files -> Buscamos el archivo que vamos a importar, este proceso lo realizaremos dos veces, una para importar la colección y la otra para importar las variables.


##  ⚙ Ejecutando las pruebas :

* Para ejecutar la colección  pasamos el mouse por la carpeta de la colección y se visualizaran tres puntos, damos clic en ellos y nos aparecera un menu donde daremos clic en la opcion de rub collection, nos aparece una pantalla con todos nuestros end point, si requerimos realizar varias veces la prueba en el campo de iterations ponemos los ciclos que deseamos ejecutar de lo contrario damos clic en run pruebaB.

![Demo petstore](http://g.recordit.co/XSNie3uBji.gif)



* Para ejecutar la colección y obtener el reporte tenemos que abrir el cmd y ejecutar la siguiente sentencia:
 
newman run ruta en donde se encuentra la colección.json ruta donde se encuentra las variables de ambiente.json --delay-request 60 --reporter-cli-no-banner --reporter-htmlextra-title "Pet Store." --reporter-htmlextra-testPaging  --reporter-htmlextra-browserTitle "Pet Store" --reporter-htmlextra-showMarkdownLinks -r htmlextra

Ejemplo:

newman run C:\Users\Eduardo_Sanchez\Documents\pruebaB.postman_collection.json --environment C:\Users\Eduardo_Sanchez\Documents\pruebaB.postman_environment.json --delay-request 60 --reporter-cli-no-banner --reporter-htmlextra-title "Pet Store." --reporter-htmlextra-testPaging  --reporter-htmlextra-browserTitle "Pet Store" --reporter-htmlextra-showMarkdownLinks -r htmlextra

![Demo reporte](http://g.recordit.co/8fpVKvuhfs.gif)


## 🔩 Pruebas end-to-end :

* Se crea un nuevo animal en la pagina de petstore.
* Se verifica que el animal nuevo se haya guardado correctamente en la base de datos.
* Se modifica un animal ya existente.

## 📜 Licencia :

* The MIT License (MIT).
