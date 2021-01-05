# Proyecto Mexflix
## Servicio de Peliculas CRUD

Este aplicacion esta basada en PHP y esta construida en base al MVC.
Programacion Orientada a Objetos. 

>Esto proyecto se realizo en base al curso de Jhonathan Mircha en donde realiza dicha aplicacion.
El nombre del curso se encuentra en Youtube como *Curso Programación Orientada a Objetos con PHP*

### Datos para logearse
User y Password


| User   | Password |
| ------ | ------   |
| @admin | admin    |
| @user  | user     |

### Conexión
Para esta aplicacion usamos MySQL 8, esta nueva version agrega un complemento de autenticacion  **caching_sha2_password**

Ingresamos a a consola de MySQL

```sh
mysql -u root -p
```

Para poder conectarse necesitamos modificar un usuario
```sql
  ALTER USER 'usuario'@'localhost'
  IDENTIFIED WITH mysql_native_password
  BY 'contraseña';
```
O crear un nuevo usuario

```sql
CREATE USER 'usuario'@'localhost'
IDENTIFIED WITH mysql_native_password BY 'contraseña';
```

###### Tenemos que cambiar los datos conexión del archivo Model.php
- **$db_user** = 'usuario'
- **$db_pass** = 'contraseña'


### Database
Dentro de la carpeta *Base de Datos*, se encuenta el archivo `mexflix_schema.sql` que necesitamos ejecutar para poder arrancar la aplicacion. 
Ingresamoa MySQL desde la consola

```sql
mysql -u root -p
SOURCE *ruta_del_archivo*
```



>**Nota**
Tener en cuenta que el nombre de la carpeta en donde se almacenara la aplicacion tiene que ser igual al nombre que se le da RewriteBase en el archivo `.htaccess`
