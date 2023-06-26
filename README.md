# Tienda en Línea

Este proyecto es una API REST desarrollada con Django y MongoDB, que sirve como backend para una tienda en línea. Proporciona endpoints para administrar clientes.

## Requisitos previos

- Python 3.x instalado en tu sistema.
- Pip (administrador de paquetes de Python) instalado.

## Configuración del entorno local

1. Clonar el repositorio:
   
   git clone https://github.com/Pablobw/BD_Avanzadas.git


2. Configurar el entorno virtual:
- Navega hasta la carpeta raíz del proyecto.
- Crea un entorno virtual ejecutando:
  ```
  python -m venv myenv
  ```
- Activa el entorno virtual:
  - En Windows:
    ```
    myenv\Scripts\activate
    ```
  - En macOS/Linux:
    ```
    source myenv/bin/activate
    ```

3. Instalar dependencias:
- Asegúrate de que estás en el entorno virtual activado.
- Ejecuta:
  ```
  pip install -r requirements.txt
  ```

4. Configurar la base de datos:
- Abre el archivo `settings.py` ubicado en la carpeta `tiendaenlinea`.
- Verifica la configuración de la base de datos en la sección `DATABASES`.
- Asegúrate de que los detalles de conexión (nombre de la base de datos, host, puerto) sean correctos.
- Guarda el archivo `settings.py`.

5. Realizar las migraciones:
- Asegúrate de que estás en el entorno virtual activado y ubicado en la carpeta raíz del proyecto.
- Ejecuta:
  ```
  python manage.py migrate
  ```

6. Iniciar el servidor de desarrollo:
- Asegúrate de que estás en el entorno virtual activado y ubicado en la carpeta raíz del proyecto.
- Ejecuta:
  ```
  python manage.py runserver
  ```

7. Acceder a la aplicación:
- Abre un navegador web.
- Visita: `http://127.0.0.1:8000/`
- Deberías ver la página de inicio de la aplicación.

## Endpoints de la API

- **GET /api/customers/**
- Retorna todos los clientes.
- Código de estado HTTP: 200 (OK)

- **POST /api/customer/**
- Crea un nuevo cliente.
- Datos del cliente deben enviarse en el cuerpo de la solicitud (body).
- Retorna los datos del nuevo cliente creado.
- Código de estado HTTP: 201 (Created)

- **GET /api/customer/<id>/**
- Retorna un cliente basado en su ID asociado.
- Si el cliente no existe, retorna un código de estado HTTP 404 (Not Found).
- Si el cliente es encontrado, retorna los datos del cliente.
- Código de estado HTTP: 200 (OK)

- **PUT /api/customer/<id>/**
- Actualiza un cliente existente.
- Si el cliente no puede ser encontrado, retorna un código de estado HTTP 404 (Not Found).
- Si el cliente es encontrado y actualizado, retorna los datos del cliente actualizado.
- Código de estado HTTP: 200 (OK)

- **DELETE /api/customer/<id>/**
- Elimina un cliente basado en su ID asociado.
- Si el cliente no existe, retorna un código de estado HTTP 404 (Not Found).
- Si el cliente es encontrado y eliminado, retorna un código de estado HTTP 204 (No Content)



