## Actualizar el Sistema
Asegúrate de que tu sistema esté actualizado antes de instalar las dependencias:
```
sudo apt update && sudo apt upgrade -y
```
### Instalar PHP y Extensiones
Laravel requiere PHP y algunas extensiones adicionales:
```
sudo apt install php php-cli php-mbstring php-xml php-zip php-curl php-intl php-mysql unzip curl -y
```
### Instalar Composer
Composer es el administrador de dependencias de PHP y necesario para instalar Laravel:
```
curl -sS https://getcomposer.org/installer | php
sudo mv composer.phar /usr/local/bin/composer
```
**Verifica la instalación:**
```
composer -v
```
## Instalar Laravel
Para instalar Laravel globalmente, ejecuta:
```
composer global require laravel/installer
```
Asegúrate de que el directorio global de Composer esté en tu $PATH:
```
echo 'export PATH="$HOME/.config/composer/vendor/bin:$PATH"' >> ~/.bashrc
source ~/.bashrc
```
## Crear un Proyecto Laravel
Ahora puedes crear un nuevo proyecto de Laravel:
```
laravel new nombre_proyecto
```
O, si prefieres usar Composer:

## Configurar Permisos
Ajusta permisos para evitar problemas con la carpeta storage y bootstrap/cache:
```
sudo chown -R $USER:www-data nombre_proyecto/storage nombre_proyecto/bootstrap/cache
sudo chmod -R 775 nombre_proyecto/storage nombre_proyecto/bootstrap/cache
```
