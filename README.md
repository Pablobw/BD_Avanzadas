# Actividad Final

## Objetivos
Los objetivos de este proyecto son:

1. Aplicar comandos básicos de MongoDB.
2. Aplicar comandos esenciales de MongoDB Shell en relación con operaciones CRUD.
3. Realizar consultas a documentos.

## Actividad

- Construir una API Rest utilizando el lenguaje de programación/framework de su preferencia y MongoDB para la persistencia de datos.
- Los end points a implementar son los siguientes:
  - `GET` => Para retornar todos los documentos de una colección.
  - `GET` => Para retornar un solo documento de una colección, basado en su ID asociado.
  - `POST` => Para crear un nuevo documento en una colección.
  - `PUT` => Para actualizar un documento de una colección.
  - `DELETE` => Para eliminar un documento de una colección.

El dominio de la colección creada es un tema libre. Si no se siente particularmente creativo, considere la situación de desempeño que se describe a continuación.

### Descripción de la Situación

tiendaenlinea.cl es un portal online que vende todo tipo de productos de retail (ropa, calzado, electrodomésticos, entre otros) para el mercado chileno.

La empresa pretende expandirse al resto de los países de Latinoamérica, para esto desean que su aplicación sea altamente escalable y resiliente, con el fin de soportar las cientos de peticiones diarias actuales, más las que provendrán de los nuevos mercados.

El nuevo stack tecnológico es el siguiente:

- Capa de presentación (vista): ReactJS, HTML 5, Javascript, CSS 3
- Capa de negocios (controlador): Rest API (Django Rest Framework)
- Capa de datos (modelo): Models (Django Rest Framework)
- Base de datos: MongoDB

### Microservicio Customer

Implemente el microservicio Customer (Cliente) mediante la creación de una API Rest con integración a base de datos.

#### Contrato Rest

|Método HTTP|URL|Descripción|
|---|---|---|
|GET|customers/|Retorna todos los clientes, si la petición es exitosa, envía un código de estado HTTP 200 (OK).|
|POST|customer/|Crea un nuevo cliente, la solicitud debe incluir los datos del nuevo cliente dentro del cuerpo (body). Si el cliente es creado retorna los datos del nuevo cliente y envía un código de estado HTTP 201 (Created).|
|GET|customer/<id>|Retorna un cliente basado en su id asociado, si el cliente no existe, envía un código de estado HTTP 404 (Not Found), en caso de ser encontrado, retorna el cliente y envía un código de estado HTTP 200 (OK).|
|PUT|customer/<id>|Actualiza un cliente existente, si el cliente no puede ser encontrado, envía un código de estado HTTP 404 (Not Found), en caso de ser encontrado y actualizado, retorna el cliente actualizado y envía un código de estado HTTP 200 (OK).|
|DELETE|customer/<id>|Elimina un cliente basado en su id asociado, si el cliente no existe, envía un código de estado HTTP 404 (Not Found), en caso de ser encontrado y eliminado, envía un código de estado HTTP 204 (No Content).|

#### Consideraciones

- El estándar de transferencia de datos a utilizar es JSON.

## Entregable

Al finalizar la actividad deberá subir a LMS el código completo de la implementación de la API y la base de datos. Además, debe proporcionar todos los pasos necesarios para levantar el proyecto en un entorno local.
