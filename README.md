# rest-master

## Getting started

Pasos para crear el RESTAPI mediante PHP SLIM:

1. Instalar PHP y APACHE (Puede ser manualmente o mediante XAMPP, MAMPP, WAMPP...)

2. Clonar el repositorio -> https://gitlab.com/usb-web-programming-autumn-2023/php/rest-master

3. Instalamos composer -> https://getcomposer.org/

4. Verificamos a través de consola que esté instalado composer -> composer -v

5. Guardamos la carpeta del proyecto en el 'htdocs' correspondiente, para Apache -> C:\apache\htdocs. para Xampp -> C:\xampp\htdocs

6. Cambiamos las variables de configuración de la base de datos -> config/db.php

7. Cambiamos las consultas a la base de datos -> customers.php

8. Hacemos el deploy local con la referencia a la API -> localhost/public/index.php/api/funcionallamar

9. Creamos el método para convertir a JSON las consultas a la db -> json_encode($variable);

## English

Hi and welcome, this repository contains the source code for a php-based web app that shows the
design and creation of a rest web service by using php slim framework.

Available online at (soon)

Code is organized as follows:

1.  A composer file for specifying the use of project libraries, in this case slim framework library.

2.  A folder named "src" which contains a configuration and routes subfolders.

         Config contains a file named db.php which manage connections to DB.
         Routes contains a file named customer.php which declare the routes to be used for the web services
         endpoints, as well as, the DB queries involved:

    a. /api/customers --> getting all the customers information from the db GET

    b. /api/customer/{id} --> getting just an user, only the information from one user, just by specifying an ID. GET

    c. /api/customer/add --> adding an user to the DB and its related information POST

    d. /api/customer/update/{id} --> updating the information from an user already created, just by using an user ID PUT

    e. /api/customer/delete/{id} --> deleting all information related to an user, just by using an user ID DELETE

3.  An index file, responsible for inoking the web app "controller" file --> customers.php

4.  A folder named sql, which contains the sqldump file from a MySQL DB.

5.  A folder named screenshots, which contains captures from the web services response (displaying json responses from the GET and POST methods).
