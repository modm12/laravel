# Laravel Iglesia

Este repositorio contiene una guía básica para iniciar una aplicación de administración de iglesia en Laravel.

## 1. Configuración inicial

1. Instala Composer: [https://getcomposer.org/download/](https://getcomposer.org/download/)
2. Crea un nuevo proyecto Laravel:
   ```bash
   composer create-project laravel/laravel iglesia
   cd iglesia
   ```
3. Configura la base de datos en `.env`:
   ```env
   DB_CONNECTION=mysql
   DB_HOST=127.0.0.1
   DB_PORT=3306
   DB_DATABASE=iglesia
   DB_USERNAME=tu_usuario
   DB_PASSWORD=tu_contraseña
   ```
4. Ejecuta las migraciones iniciales:
   ```bash
   php artisan migrate
   ```

## 2. Funcionalidades principales

### Gestión de miembros
- Crea el modelo y la migración:
  ```bash
  php artisan make:model Miembro -m
  ```
- Controlador y rutas:
  ```bash
  php artisan make:controller MiembroController --resource
  ```

### Gestión de eventos
- Modelo y migración:
  ```bash
  php artisan make:model Evento -m
  ```
- Controlador y rutas:
  ```bash
  php artisan make:controller EventoController --resource
  ```

### Donaciones y finanzas
- Modelo de Donación:
  ```bash
  php artisan make:model Donacion -m
  ```

### Grupos o ministerios
- Modelo de Grupo:
  ```bash
  php artisan make:model Grupo -m
  ```

### Autenticación y roles
- Instala Breeze:
  ```bash
  composer require laravel/breeze --dev
  php artisan breeze:install
  npm install && npm run dev
  ```

## 3. Buenas prácticas

- Utiliza migraciones y validación.
- Implementa notificaciones y pruebas con `php artisan test`.
- Configura roles y permisos usando `spatie/laravel-permission`.

## 4. Despliegue

- Mantén tus dependencias actualizadas y realiza respaldos regulares.

