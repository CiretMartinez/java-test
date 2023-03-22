# Desafio Back End Java na DoroTech

REST API MongoDB java test

El siguiente proyecto Maven responde a un API de servicios rest para el manejo de una coleccion de productos.

Lenguaje de programacion: Java Version 17 Manejador de base de datos NoSql MongoDB Framework Springframework

## Build

mvn clean install

## Run the app

Correr la clase main Application.java

## REST API

### Obtener lista de todos los productos

Request

GET /products

Response

Date: Wed, 22 Mar 2023 18:50:38 GMT Status: 200 OK Content-Type: application/json

[
    {
        "_id": "641a551061fa46a03dc066fb",
        "name": "Producto_prueba",
        "description": "Producto de prueba ap",
        "price": 30.5,
        "amount": 10 
    }, 
    {
        "_id": "641b2c5cef2db43fec2ac34f",
        "name": "Producto_prueba_postman",
        "description": "Producto de prueba postman",
        "price": 100.0,
        "amount": 5 
    }
]

### Crear un nuevo producto

Request

POST /products

Body

{
    "name": "Producto_prueba",
    "description": "Producto de prueba ap",
    "price": 30.5,
    "amount": 10
}

Response

Date: Wed, 22 Mar 2023 18:55:09 GMT Status: 200 OK Content-Type: application/json

{
    "_id": "641b4f0d7e64ed4523347c97",
    "name": "Producto_prueba",
    "description": "Producto de prueba ap",
    "price": 30.5,
    "amount": 10
}

### Obtener un producto por ID

Request

GET /products/641b4f0d7e64ed4523347c97

Response

Date: Wed, 22 Mar 2023 18:59:09 GMT Status: 200 OK Content-Type: application/json

{
    "_id": "641b4f0d7e64ed4523347c97",
    "name": "Producto_prueba",
    "description": "Producto de prueba ap",
    "price": 30.5,
    "amount": 10
}

### Eliminar un producto en particular

Request

DELETE /products/641b4f0d7e64ed4523347c97

Response

Date: Wed, 22 Mar 2023 19:02:17 GMT Status: 200 OK Content-Type: application/json

