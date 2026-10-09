# Sistema Courier - Alexa Courier

Sistema web de gestión para **Alexa Courier**, desarrollado con **Laravel 12**. Permite administrar las operaciones del negocio desde un solo lugar:

-  Ventas, compras y comprobantes
-  Clientes y proveedores
-  Productos, categorías, marcas y presentaciones
-  Inventario y kardex
-  Cajas y movimientos
-  Empleados, usuarios, roles y permisos
-  Reportes en PDF y Excel
-  Registro de actividad del sistema

## Dependencias

-  Se debe tener instalado [XAMPP](https://www.apachefriends.org/es/download.html "XAMPP") (versión **PHP** **8.2** o superior)

-  Se debe tener instalado [Composer](https://getcomposer.org/download/ "Composer")

  

## Como instalar en Local

1.  Clone  o  descargue  el  repositorio  a  una  carpeta  en  Local

  

1.  Abra  el  repositorio  en  su  editor  de  código  favorito  (**Visual  Studio  Code**)

  

1.  Ejecute  la  aplicación  **XAMPP**  e  inice  los  módulos  de  **Apache**  y  **MySQL**

  

1.  Abra  una  nueva  terminal  en  su  editor

  

1.  Compruebe  de  que  tiene  instalado  todas  dependencias  correctamente,  ejecute  los  siguientes  comandos:  **(Ambos  comandos  deberán  ejecutarse  correctamente  -  ejecutar  en  la  terminal)**

```bash

php  -v

```

```bash

composer  -v

```

  

1.  Ahora  ejecute  los  comandos  para  la  configuración  del  proyecto  (**ejecutar  en  la  terminal**):

  

-  Este comando nos va a instalar todas la dependencias de composer

```bash

composer install

```

-  En el directorio raíz encontrará el arhivo **.env.example**, dupliquelo, al archivo duplicado cambiar de nombre como **.env**, este archivo se debe modificar según las configuraciones de nuestro proyecto. Ahí se muestran como debería quedar

```bash

DB_CONNECTION=mysql

DB_HOST=127.0.0.1

DB_PORT=3306

DB_DATABASE=dbsistemaventas

DB_USERNAME=root

DB_PASSWORD=

```

-  Ejecutar el comando para crear la Key de seguridad

```bash

php artisan key:generate

```

-  Ingrese al administrador de [PHP MyAdmin](http://localhost/phpmyadmin/) y cree una nueva base de datos, el nombre es opcional, pero por defecto nombrarla **dbsistemaventas**

  

-  Correr la migraciones del proyecto

```bash

php artisan migrate

```

-  Ejecute los seeders, esto creará un usuario administrador, puede revisar las credenciales en el archivo (**database/seeders/UserSeeder**)

```bash

php artisan db:seed

```

-  Corra comando para crear el enlace simbólico

```bash

php artisan storage:link

```
-  Si quiere ejecutar los trabajos (modo de desarrollo)

```bash

php artisan queue:listen

```

  -  Ejecute el proyecto (en otra terminal)

```bash

php artisan serve

```

## Notas

-  Este sistema está basado en un proyecto de punto de venta de código abierto, puede obtener más información sobre el proyecto base [aquí](https://universityproyectx.blogspot.com/2022/10/sistema-de-ventas-web-minersa-srl.html).

- [FAQ sobre el proyecto base](https://universityproyectx.blogspot.com/2023/06/faq-sobre-el-sistema-de-ventas-de.html)

  

------------

![Img](https://github.com/SakNoelCode/Imagenes_Proyectos/blob/master/sistema-ventas-captura.png)
