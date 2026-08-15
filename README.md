# Aplicación de Restaurante

**Estudiante:** Masculino Conejo Janneth Talía

**Asignatura:** Programación Orientada a Objetos  
**Semana:** 9

## Descripción

Restaurante App es una aplicación desarrollada en Python utilizando Programación Orientada a Objetos (POO). El proyecto representa la administración básica de un restaurante mediante una aplicación de consola.

El sistema permite administrar productos, usuarios y categorías de productos.

Las principales operaciones sobre productos son:

- Registrar productos.
- Buscar productos.
- Actualizar productos.
- Eliminar productos.
- Listar productos.

También permite:

- Registrar usuarios.
- Listar usuarios.
- Mostrar las categorías únicas de los productos.

La aplicación mantiene una arquitectura modular separando los modelos, el servicio encargado de administrar las colecciones y el punto de entrada del programa.

## Estructura del proyecto

    restaurante_app/
    ├── modelos/
    │   ├── __init__.py
    │   ├── producto.py
    │   └── usuario.py
    ├── servicios/
    │   ├── __init__.py
    │   └── restaurante.py
    ├── main.py
    └── README.md

## Responsabilidad de los componentes

### modelos/producto.py

Contiene la clase Producto, que representa un producto del restaurante.

Maneja información como:

- Código.
- Nombre.
- Categoría.
- Precio.
- Disponibilidad.

### modelos/usuario.py

Contiene la clase Usuario, que representa a una persona registrada en el sistema.

Maneja información como:

- Identificación.
- Nombre.
- Correo electrónico.

### servicios/restaurante.py

Contiene la clase Restaurante, encargada de administrar las colecciones de productos y usuarios.

Sus principales responsabilidades son:

- Registrar productos.
- Buscar productos.
- Actualizar productos.
- Eliminar productos.
- Listar productos.
- Registrar usuarios.
- Listar usuarios.
- Evitar códigos de productos duplicados.
- Evitar identificaciones de usuarios duplicadas.
- Obtener las categorías únicas de los productos.

### main.py

Es el punto de entrada del programa y se encarga de la interacción con el usuario mediante un menú de consola.

Sus principales responsabilidades son:

- Mostrar el menú principal.
- Solicitar información mediante input().
- Crear objetos Producto y Usuario.
- Utilizar los métodos de Restaurante.
- Mostrar los resultados al usuario.
- Controlar las opciones del menú.
- Manejar entradas incorrectas.

### README.md

Contiene la documentación del proyecto, su estructura, funcionamiento y explicación de las estructuras de datos utilizadas.

## Estructuras de datos utilizadas

### Lista (list)

Las listas se utilizan en la clase Restaurante para almacenar los productos y usuarios registrados.

Se utilizan principalmente:

- Una lista de productos.
- Una lista de usuarios.

Las listas son adecuadas porque estas colecciones pueden aumentar o disminuir durante la ejecución del programa.

También permiten realizar las operaciones de registro, búsqueda, actualización, eliminación y listado de productos.

### Tupla (tuple)

En main.py se utiliza la tupla OPCIONES_MENU para almacenar las opciones principales del menú.

La tupla es adecuada porque las opciones del menú permanecen estables durante la ejecución del programa y no necesitan modificarse.

### Diccionario (dict)

En main.py se utiliza un diccionario mediante la función obtener_acciones_menu().

Este diccionario relaciona cada número del menú con el nombre de la operación correspondiente.

Por ejemplo:

    "1" → "registrar_producto"
    "2" → "buscar_producto"
    "3" → "actualizar_producto"

De esta manera se establece una relación clara de clave → valor para organizar las acciones disponibles en el menú.

### Conjunto (set)

Se utiliza un conjunto en Restaurante para obtener las categorías de los productos sin elementos repetidos.

Por ejemplo, si existen varios productos de la categoría Bebidas, esta categoría solamente se muestra una vez.

El conjunto permite obtener y mostrar únicamente las categorías únicas registradas en el sistema.

## Funcionalidades

El sistema cuenta con las siguientes opciones:

1. Registrar producto.
2. Buscar producto.
3. Actualizar producto.
4. Eliminar producto.
5. Listar productos.
6. Registrar usuario.
7. Listar usuarios.
8. Mostrar categorías.
9. Salir.

### Productos

El sistema permite registrar productos ingresando su código, nombre, categoría, precio y disponibilidad.

También permite buscar un producto mediante su código, actualizar sus datos, eliminarlo y mostrar todos los productos registrados.

El sistema controla que no existan códigos de productos duplicados.

### Usuarios

El sistema permite registrar usuarios ingresando su identificación, nombre y correo electrónico.

También permite listar los usuarios registrados.

El sistema controla que no existan identificaciones de usuarios duplicadas.

### Categorías

El sistema permite mostrar las categorías de los productos sin elementos duplicados mediante el uso de un conjunto (set).

## Validaciones

El sistema realiza diferentes validaciones para mantener la información correcta.

Entre ellas:

- Evitar códigos de productos duplicados.
- Evitar identificaciones de usuarios duplicadas.
- Validar el ingreso del precio.
- Evitar códigos vacíos.
- Controlar opciones incorrectas del menú.
- Verificar que un producto exista antes de actualizarlo o eliminarlo.
- Manejar errores mediante excepciones cuando corresponde.

## Instrucciones para ejecutar el programa

### Requisitos

Para ejecutar el proyecto se necesita:

- Python 3.
- Visual Studio Code u otro editor compatible con Python.
- Terminal o consola.

## Separación de responsabilidades

El proyecto mantiene una separación entre los diferentes componentes:

- modelos/ contiene las clases Producto y Usuario.
- servicios/ contiene la clase Restaurante, encargada de administrar las colecciones y operaciones.
- main.py se encarga de la interacción con el usuario.
- README.md contiene la documentación del proyecto.

La administración de las colecciones se mantiene dentro de Restaurante.

De esta manera, main.py no modifica directamente las listas internas del servicio, sino que utiliza los métodos proporcionados por la clase Restaurante.

## Reflexión

Seleccionar correctamente una estructura de datos es importante porque cada estructura está diseñada para resolver diferentes necesidades.

En este proyecto, las listas permiten almacenar colecciones dinámicas de productos y usuarios.

Las tuplas permiten mantener información estable, como las opciones del menú.

Los diccionarios permiten relacionar una clave con un valor y organizar las acciones del menú.

Los conjuntos permiten trabajar con información única, como las categorías de los productos.

Elegir la estructura adecuada permite que el programa sea más organizado, fácil de comprender, mantener y ampliar en el futuro.
