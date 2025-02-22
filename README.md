# objetivo: 
Poner en práctica cómo interconectar clases, para poder interactuar entre ellas, pasando una instancia de clase como argumento.

# Sistema de Biblioteca

Este proyecto modela un sistema básico para manejar libros en una biblioteca. El programa permite agregar y listar libros mediante una interfaz de usuario interactiva.

## Clases del Sistema

1. **Libro**: Representa los libros con atributos como título y autor.
2. **Biblioteca**: Maneja una lista de libros y proporciona métodos para agregar y mostrar libros.
3. **InterfazUsuario**: Interactúa con el usuario para permitir agregar y mostrar libros.

## Requisitos del ejercicio

- La clase `Biblioteca` tiene métodos para agregar libros y mostrar la lista de libros.
- La clase `InterfazUsuario` interactúa con el usuario y utiliza los métodos de `Biblioteca`.
- La interacción entre las clases se realiza pasando la instancia de una clase como argumento a la otra.

## Cómo usar

1. El sistema muestra un menú donde el usuario puede elegir entre:
   - **Agregar un libro**: El usuario ingresa el título y autor, y el libro se agrega a la biblioteca.
   - **Mostrar libros**: Muestra una lista de todos los libros agregados.
   - **Salir**: Termina el programa.
   
## Ejemplo

```python
# Crear la instancia de la biblioteca
biblioteca = Biblioteca()

# Crear la interfaz de usuario
interfaz = InterfazUsuario(biblioteca)

# Iniciar el menú de usuario
interfaz.menu()
```

### Explicación del código

El código consta de tres clases principales:

1. **Clase `Libro`**: 
   - Tiene dos atributos, `titulo` y `autor`, que representan la información básica de un libro.
   - El método `__str__` permite mostrar el libro en formato de texto cuando se imprime un objeto de esta clase, mostrando el título y autor de manera legible.

2. **Clase `Biblioteca`**:
   - Esta clase gestiona una lista llamada `libros`, donde se almacenan los objetos `Libro`.
   - El método `agregar_libros` permite añadir un nuevo libro a esta lista.
   - El método `mostrar_libros` recorre la lista y muestra los detalles de cada libro. Si no hay libros en la lista, imprime un mensaje indicando que está vacía.

3. **Clase `InterfazUsuario`**:
   - Recibe una instancia de la clase `Biblioteca` como parámetro en su constructor, lo que le permite interactuar con los libros de la biblioteca.
   - Su método `menu` muestra las opciones al usuario en un ciclo continuo hasta que se elige la opción de salir. 
   - El método `agregar_libro` permite al usuario ingresar el título y autor de un libro, luego crea un objeto `Libro` y lo agrega a la biblioteca.

### Flujo de interacción
El flujo de ejecución es el siguiente:
- Se crea una instancia de `Biblioteca` que contendrá los libros.
- Se crea una instancia de `InterfazUsuario`, que gestionará la interacción con el usuario y tomará la biblioteca como argumento.
- El usuario puede elegir entre agregar libros, ver los libros almacenados o salir del programa.

Este enfoque modular permite añadir fácilmente más funcionalidades, como la eliminación de libros o la búsqueda por autor, sin afectar el diseño general del sistema.



