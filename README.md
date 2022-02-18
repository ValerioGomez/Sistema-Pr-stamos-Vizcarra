# Sistema-Pr-stamos-Vizcarra
Sistema de Préstamos con Laravel MYSQL para desplegar en Heroku.
Cliente: RapidCash
### Instalación
Ejecutar los siguientes comandos en orden
```cmd
git clone https://github.com/leifermendez/sistema-prestamos.git
```
```cmd
cd sistema-prestamos
```
```cmd
composer install
```
Seguidamente recuerda que por seguridad el archivo <b>"<em>.env</em>"</b> no se copia, para ello dispones del mismo pero con el nombre
<b>"<em>.env.example</em>"</b> el cual deberás renombrar a <b>"<em>.env</em>"</b> solamente.

Recuerda también ingresar en el archivo <b>"<em>.env</b>"</em> los datos de conexión a la base de datos que deberas haber creado previamente, esto es importante para poder continuar con el siguiente paso y generar el <b>"<em>key</b>"</em>.
```cmd
php artisan key:generate
```
```cmd
php artisan migrate:install
```
```cmd
php artisan migrate
```
```cmd
php artisan db:seed
php artisan migrate:fresh --seed
php artisan serve
```

Optimiza el funcionamiento de las fechas estableciendo tu zona horaria [Ver zonas horarias](https://www.php.net/manual/es/timezones.php)

__config/app.php__
```php
    ....
    'timezone' => 'Europe/Madrid',
    ....
```

__NOTA:__ Recuerda para un optimo funcionamiento en modo PRODUCCION en el archivo `.env` establece
 los siguientes valores de esta manera se desactiva los logs.
```
APP_ENV=production
APP_DEBUG=false
```


### Usurios
Luego de correr con exito la migracion y los seeders, el sistema crea varios usuarios para comenzar a probar

__Rol__: `admin`
__User__:`admin@admin.com`
__Contraseña__:`12345678`


__Rol__: `supervisor`
__User__:`supervisor@supervisor.com`
__Contraseña__:`12345678`


__Rol__: `agente`
__User__:`agente@agente.com`
__Contraseña__:`12345678`
