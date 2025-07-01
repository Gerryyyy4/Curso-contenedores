# Proyecto Final Curso Contenedores

## Instrucciones de ejecucion



# DistribuTech Solutions - Sistema de Gestión de Inventario Empresarial

## Descripción

DistribuTech Solutions es una empresa de distribución de productos tecnológicos con un catálogo extenso. Este proyecto moderniza su infraestructura tecnológica, permitiendo a clientes externos consultar el catálogo, a empleados gestionar inventario y a una API centralizada manejar la lógica de negocio.

## Arquitectura del Sistema

```
Internet → nginx (Reverse Proxy) → {
├── Web Pública (Puerto 3001)
├── Web Administrativa (Puerto 3002)
└── API REST (Puerto 3003)
}
↓
Base de Datos MySQL (Puerto 3306)
```

## Componentes

1. **Nginx - Reverse Proxy**: Enruta peticiones a los servicios correspondientes (catálogo, administración, API).
2. **Web Pública**: Catálogo de productos accesible para clientes externos.
3. **Web Administrativa**: Herramienta para la gestión de inventario de los empleados.
4. **API REST**: Lógica de negocio, gestionando operaciones CRUD de productos y estadísticas.
5. **Base de Datos MySQL**: Contiene la información de los productos.

## Requisitos

1. Docker
2. Docker Compose

## Instalación

1. Clonar el repositorio:
   ```bash
   git clone https://github.com/Gerryyyy4/Curso-contenedores.git
    ```

2. Construir y ejecutar los contenedores con Docker Compose:

   ```bash
   docker-compose up --build
   ```
3. Acceder a las siguientes URLs:

   * **Catálogo público**: `http://localhost`
   * **Panel administrativo**: `http://localhost/admin`
   * **API REST**: `http://localhost/api/productos`

## Estructura del Proyecto

```
proyecto-final/
├── nginx/
│   ├── nginx.conf                 # Configuración del reverse proxy
├── web-publica/
│   ├── index.html                 # Catálogo público
├── web-admin/
│   ├── index.html                 # Panel administrativo
├── api/
│   ├── app.py                     # API REST en Python Flask
└── database/
    └── init.sql                   # Script de inicialización de BD
```

## Funcionalidades

* **Web Pública**: Ver productos, buscar y filtrar productos.
* **Web Administrativa**: Dashboard, agregar/editar productos, alertas de stock bajo.
* **API REST**: CRUD de productos, estadísticas de inventario.



