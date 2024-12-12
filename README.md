# Introducción a Python

## Índice

1. [Introducción](#1-introducción)
2. [Conceptos Fundamentales](#2-conceptos-fundamentales)
3. [Sintaxis Básica](#3-sintaxis-básica)
4. [Estructuras de Control](#4-estructuras-de-control)
5. [Funciones](#5-funciones)
6. [Estructuras de Datos](#6-estructuras-de-datos)
7. [Ejercicio Práctico](#7-ejercicio-práctico)
8. [Recursos Adicionales](#8-recursos-adicionales)

---

## 1. Introducción

Python es un lenguaje de programación de alto nivel, interpretado y de propósito general. Es conocido por su simplicidad y legibilidad, lo que lo hace ideal tanto para principiantes como para desarrolladores experimentados.

🚀 Python se utiliza en una amplia variedad de aplicaciones, desde desarrollo web y análisis de datos hasta inteligencia artificial y aprendizaje automático.

👨‍💻 Creado por Guido van Rossum y lanzado por primera vez en 1991, Python ha crecido para convertirse en uno de los lenguajes de programación más populares del mundo.

💻 Python enfatiza la legibilidad del código y utiliza la indentación para delimitar bloques de código, lo que fomenta un estilo de programación limpio y consistente.

🚨 ¿Entendemos por qué Python es un buen lenguaje para aprender programación? ¿Qué ventajas ofrece sobre otros lenguajes? 🚨

---
### 🛠 Instalación

### Windows

En Windows, sigue estos pasos para instalar Python:

1. Ve al sitio oficial de Python y descarga el instalador: [Descargar Python](https://www.python.org/downloads/).
2. Ejecuta el instalador y asegúrate de marcar la opción **"Add Python to PATH"** antes de hacer clic en **"Install Now"**.
3. Completa el proceso de instalación siguiendo las instrucciones del instalador.


### macOS

macOS viene con Python preinstalado, pero generalmente es una versión antigua. Para instalar la última versión:

1. Instala Homebrew (si aún no lo tienes):

    /bin/bash -c "$(curl -fsSL [https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh](https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh))"

2. Instala Python usando Homebrew:

    ```plaintext
    brew install python
    ```

3. Verifica la instalación:

    ```plaintext    
    python3 --version
    ```

### Linux
La mayoría de las distribuciones de Linux vienen con Python preinstalado. Para instalar la última versión:

#### Ubuntu o Debian:

```plaintext
sudo apt update
sudo apt install python3 python3-pip
```

### Verificación de la Instalación
Después de la instalación, puedes verificar que Python esté correctamente instalado abriendo una terminal (Símbolo del Sistema en Windows) y escribiendo:

```plaintext
python --version

python3 --version
```

Esto debería mostrar la versión de Python instalada.

---

## 2. Conceptos Fundamentales

🔢 **Variables**: Contenedores para almacenar datos.

🧮 **Tipos de Datos**: Incluyen enteros, flotantes, cadenas, booleanos, etc.

🔀 **Operadores**: Símbolos que realizan operaciones en variables y valores.

📦 **Funciones**: Bloques de código reutilizables que realizan tareas específicas.

🗃️ **Módulos**: Archivos que contienen definiciones y declaraciones de Python.

🔄 **Bucles**: Estructuras que permiten la ejecución repetida de código.

🔀 **Condicionales**: Permiten la ejecución de diferentes bloques de código basados en condiciones.

## 3. Sintaxis Básica

Python utiliza indentación para definir bloques de código. Aquí hay algunos ejemplos de sintaxis básica:

```python
# Esto es un comentario

# Variables y tipos de datos
nombre = "Alice"  # Cadena
edad = 30         # Entero
altura = 1.65     # Flotante
es_estudiante = True  # Booleano

# Imprimir en la consola
print("Hola, mundo!")

# Operaciones básicas
suma = 5 + 3
resta = 10 - 4
multiplicacion = 6 * 2
division = 15 / 3

# Entrada del usuario
nombre_usuario = input("Ingrese su nombre: ")
print(f"Hola, {nombre_usuario}!")
```

## 4. Estructuras de Control

### Condicionales

```python
edad = 18

if edad >= 18:
    print("Eres mayor de edad")
elif edad >= 13:
    print("Eres un adolescente")
else:
    print("Eres un niño")
```

### Bucles

```python
# Bucle for
for i in range(5):
    print(i)

# Bucle while
contador = 0
while contador < 5:
    print(contador)
    contador += 1
```

## 5. Funciones

```python
def saludar(nombre):
    return f"Hola, {nombre}!"

mensaje = saludar("Alice")
print(mensaje)

# Función con valores por defecto
def potencia(base, exponente=2):
    return base ** exponente

print(potencia(3))    # Imprime 9
print(potencia(3, 3)) # Imprime 27
```

## 6. Estructuras de Datos

### Listas

```python
frutas = ["manzana", "banana", "cereza"]
print(frutas[0])  # Imprime "manzana"
frutas.append("naranja")
print(len(frutas))  # Imprime 4
```

### Diccionarios

```python
persona = {
    "nombre": "Bob",
    "edad": 30,
    "ciudad": "Nueva York"
}
print(persona["nombre"])  # Imprime "Bob"
persona["profesion"] = "Ingeniero"
```

### Tuplas

```python
coordenadas = (10, 20)
x, y = coordenadas
print(f"X: {x}, Y: {y}")
```

## 7. Ejercicio Práctico

Vamos a crear un programa que simule una calculadora simple. Este ejercicio utilizará funciones, estructuras de control y entrada del usuario.

```python
def suma(a, b):
    return a + b

def resta(a, b):
    return a - b

def multiplicacion(a, b):
    return a * b

def division(a, b):
    if b != 0:
        return a / b
    else:
        return "Error: División por cero"

def calculadora():
    print("Bienvenido a la calculadora simple")
    print("Operaciones disponibles:")
    print("1. Suma")
    print("2. Resta")
    print("3. Multiplicación")
    print("4. División")

    while True:
        opcion = input("Seleccione una operación (1-4) o 'q' para salir: ")
        
        if opcion == 'q':
            print("Gracias por usar la calculadora. ¡Hasta luego!")
            break

        if opcion not in ['1', '2', '3', '4']:
            print("Opción no válida. Por favor, intente de nuevo.")
            continue

        num1 = float(input("Ingrese el primer número: "))
        num2 = float(input("Ingrese el segundo número: "))

        if opcion == '1':
            print(f"Resultado: {suma(num1, num2)}")
        elif opcion == '2':
            print(f"Resultado: {resta(num1, num2)}")
        elif opcion == '3':
            print(f"Resultado: {multiplicacion(num1, num2)}")
        elif opcion == '4':
            print(f"Resultado: {division(num1, num2)}")

        print()  # Línea en blanco para mejor legibilidad

if __name__ == "__main__":
    calculadora()
```

### Explicación del Ejercicio

1. Definimos funciones para cada operación matemática básica.
2. La función `calculadora()` es el punto de entrada principal del programa.
3. Utilizamos un bucle `while` para mantener la calculadora en funcionamiento hasta que el usuario decida salir.
4. Empleamos estructuras condicionales (`if`, `elif`) para manejar diferentes opciones y casos de error.
5. Usamos `input()` para obtener datos del usuario y `float()` para convertir las entradas a números decimales.
6. La cláusula `if __name__ == "__main__":` asegura que la función `calculadora()` solo se ejecute si el script se está ejecutando directamente (no importado como módulo).

Este ejercicio demuestra el uso de varios conceptos de Python:

- Definición y uso de funciones
- Estructuras de control (bucles y condicionales)
- Manejo de entrada/salida del usuario
- Conversión de tipos de datos
- Uso de operadores aritméticos

🚨 ¿Entendemos cómo funciona cada parte del programa y cómo se combinan los conceptos de Python para crear una aplicación funcional? 🚨

## 9. Recursos Adicionales

- [Documentación oficial de Python](https://docs.python.org/3/) - La fuente definitiva para la documentación de Python.
- [Python para Principiantes](https://www.python.org/about/gettingstarted/) - Guía oficial de Python para comenzar.
- [Real Python](https://realpython.com/) - Tutoriales y artículos para todos los niveles.
- [PyCharm](https://www.jetbrains.com/pycharm/) - Un potente IDE para desarrollo en Python.
- [Python Tutor](http://pythontutor.com/) - Visualiza la ejecución de código Python paso a paso.
- [Curso de Python de Cisco con Badget (30 horas)](https://www.netacad.com/courses/python-essentials-1?courseLang=en-US)
- [Curso de introducción de Microsoft (4 horas)](https://learn.microsoft.com/es-es/training/paths/beginner-python/)
- [Curso de Python para IA y machine gratuito con certificado (3 semana)](https://ti.to/saturdaysai/python-4-ai-program)
- [Katas](https://www.codewars.com/)
- [Ejercicios](https://www.w3schools.com/python/default.asp)
