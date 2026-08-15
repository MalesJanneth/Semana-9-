# Restaurante App

**Estudiante:** Males Conejo Janneth Talía

## Semana 9 - Programación Orientada a Objetos

## Descripción

Restaurante App es una aplicación desarrollada en Python utilizando Programación Orientada a Objetos (POO).
El proyecto representa la administración básica de un restaurante mediante una aplicación de consola. En esta versión se incorporan estructuras de datos fundamentales de Python para administrar colecciones de objetos y datos del sistema.

El sistema permite administrar:

- Productos.
- Usuarios.
- Categorías de productos.

Las operaciones principales sobre productos son:

- Registrar.
- Buscar.
- Actualizar.
- Eliminar.
- Listar.

También permite:

- Registrar usuarios.
- Listar usuarios.
- Mostrar las categorías únicas de los productos.

La aplicación mantiene una arquitectura modular separando los modelos, el servicio encargado de administrar las colecciones y el punto de entrada del programa.

---

# Estructura del proyecto

```text
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

---
# Estructura del proyecto

**Lista (list)**

Se utilizan listas en Restaurante para almacenar los productos y usuarios registrados.

Lista de productos.
Lista de usuarios.

Se utilizan porque estas colecciones pueden aumentar o disminuir durante la ejecución del programa.

**Tupla (tuple)**

En main.py se utiliza la tupla OPCIONES_MENU para almacenar las opciones principales del menú.

La tupla es adecuada porque las opciones del menú permanecen estables durante la ejecución del programa.

**Diccionario (dict)**

En main.py se utiliza un diccionario mediante obtener_acciones_menu().

Este relaciona cada número del menú con el nombre de la operación correspondiente. Por ejemplo, la opción "1" se relaciona con "registrar_producto".

Esto permite organizar las opciones del menú mediante una relación clave → valor.

**Conjunto (set)**

Se utiliza un conjunto en Restaurante para obtener las categorías de productos sin repetir.

Por ejemplo, si existen varios productos de la categoría "Bebidas", esta categoría solamente se muestra una vez.

# Funcionalidades

El sistema cuenta con las siguientes opciones:

========================================
        SISTEMA DE RESTAURANTE
========================================
1. Registrar producto
2. Buscar producto
3. Actualizar producto
4. Eliminar producto
5. Listar productos
----------------------------------------
6. Registrar usuario
7. Listar usuarios
----------------------------------------
8. Mostrar categorías
9. Salir

También se realizan validaciones para evitar códigos de productos e identificaciones de usuarios duplicados y controlar entradas incorrectas.

## Refelexión

Seleccionar correctamente una estructura de datos es importante porque cada estructura está diseñada para resolver diferentes necesidades.

En este proyecto, las listas son útiles para almacenar colecciones dinámicas de productos y usuarios. Las tuplas permiten mantener información estable como las opciones del menú. Los diccionarios permiten relacionar una clave con un valor y organizar las acciones del menú. Los conjuntos permiten trabajar con información única, como las categorías de productos.

Elegir la estructura adecuada permite que el programa sea más organizado, fácil de comprender y sencillo de mantener.