# AdminBD

Aplicación PHP para administrar comercios y actividades turísticas con una base de datos MySQL o MariaDB.

## Requisitos

- PHP con las extensiones PDO y PDO MySQL
- MySQL o MariaDB
- Un servidor web local, por ejemplo XAMPP

## Configuración

1. Crea la base de datos y sus tablas ejecutando `schema.sql` en MySQL o MariaDB.
2. Configura la conexión de base de datos en `includes/db.php` para tu entorno local.
3. Define una contraseña segura para el administrador inicial y ejecuta el script desde una terminal.

En PowerShell:

```powershell
$env:ADMIN_INITIAL_PASSWORD = "elige-una-contrasena-segura"
php setup_admin.php
```

El script crea el usuario inicial `admin` si todavía no existe. No uses una contraseña real en archivos versionados ni en comandos guardados en el historial de la terminal.

## Respaldo de base de datos

`database_backup.sql` se excluye del control de versiones porque los respaldos pueden contener datos personales y credenciales cifradas. Genera un respaldo local desde la aplicación o con las herramientas de MySQL; no publiques respaldos reales.

## Seguridad

Esta aplicación está pensada para desarrollo local. Antes de desplegarla públicamente, configura credenciales de base de datos seguras, desactiva o elimina scripts de instalación y respaldo que no necesites, y usa HTTPS.
