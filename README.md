# NginX + WordPress en Docker

Este proyecto configura un servidor NginX con WordPress utilizando Docker y Docker Compose.

## 📌 Requisitos

* Docker
* Docker Compose

## 🚀 Instalación

1. Clona este repositorio:
   

```sh
   git clone https://github.com/k1ltr0h/WP-NginX-Docker.git
   cd WP-NginX-Docker
   ```

2. Copia el archivo de ejemplo y configura las variables necesarias:
   

```sh
   cp .env.example .env
   ```

3. Construye y levanta los contenedores:
   

```sh
   docker-compose up -d --build
   ```

4. Accede a WordPress en el navegador:
   

```
   http://localhost
   ```

## 🛠️ Configuración de Servicios

El stack incluye:
* **NginX** como servidor web
* **WordPress** con PHP
* **MySQL** como base de datos

### 📂 Estructura del Proyecto

```
.
├── docker-compose.yml
├── nginx/
|   |__ssl
|   |   |__cerificate.crt
|   |   |__private.key
|   |
│   ├── nginx.conf
|
└── .env.example
```

## 📜 Variables de Entorno

Asegúrate de definir correctamente el archivo `.env` :

```ini
WORDPRESS_DB_NAME=wordpress
WORDPRESS_DB_USER=user
WORDPRESS_DB_PASSWORD=secret
MYSQL_ROOT_PASSWORD=rootpassword
```

## 🔄 Comandos Útiles

* Parar los contenedores:
  

```sh
  docker-compose down
  ```

* Ver logs de los contenedores:
  

```sh
  docker-compose logs -f
  ```

* Reconstruir contenedores:
  

```sh
  docker-compose up --build -d
  ```

## 📝 Notas

* Asegúrate de que los puertos no estén en uso antes de levantar los servicios.
* Puedes modificar la configuración de NginX en `nginx/nginx.conf`.

## 📖 Licencia

Este proyecto está bajo la licencia MIT.
