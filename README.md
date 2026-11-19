# Python
Variables y Estructuras

# 🐍 PYTHON — VARIABLES Y ESTRUCTURAS

Repositorio de estudio y consulta sobre los fundamentos de programación con Python. Contiene conceptos, sintaxis, ejemplos y estructuras fundamentales del lenguaje.

---

## 📚 ÍNDICE

1. [Introducción a Python](#-1-introducción-a-python)
2. [Variables](#-2-variables)
3. [Tipos de datos](#-3-tipos-de-datos)
4. [Conversión de tipos](#-4-conversión-de-tipos)
5. [Operadores](#-5-operadores)
6. [Entrada y salida de datos](#-6-entrada-y-salida-de-datos)
7. [Estructuras condicionales](#-7-estructuras-condicionales)
8. [Estructuras repetitivas](#-8-estructuras-repetitivas)
9. [Estructuras de datos](#-9-estructuras-de-datos)
10. [Funciones](#-10-funciones)
11. [Manejo de excepciones](#-11-manejo-de-excepciones)
12. [Buenas prácticas](#-12-buenas-prácticas)

---

## 🐍 1. INTRODUCCIÓN A PYTHON

Python es un lenguaje de programación de alto nivel, interpretado y de propósito general. Se caracteriza por su sintaxis sencilla y legible.

### Características principales

- Sintaxis clara y fácil de comprender.
- Tipado dinámico.
- Lenguaje interpretado.
- Programación estructurada y orientada a objetos.
- Amplio ecosistema de bibliotecas.
- Uso en desarrollo web, automatización, análisis de datos e inteligencia artificial.

### Primer programa

```python
print("Hola, mundo")
```

`print()` permite mostrar información en la consola.

### Comentarios

```python
# Comentario de una sola línea

"""
Comentario
de varias líneas
"""
```

Los comentarios permiten documentar el código y explicar su funcionamiento.

---

## 📦 2. VARIABLES

Una variable es un identificador que permite almacenar y utilizar un dato durante la ejecución de un programa.

### Declaración de variables

```python
nombre = "Carlos"
edad = 20
altura = 1.80
activo = True
```

Python no requiere declarar previamente el tipo de dato.

### Reglas para nombrar variables

- Deben comenzar con una letra o guion bajo `_`.
- No pueden comenzar con números.
- No pueden contener espacios.
- No deben utilizar palabras reservadas del lenguaje.
- Python distingue entre mayúsculas y minúsculas.

```python
nombre_usuario = "Carlos"  # Correcto
edad2 = 20                 # Correcto
_nombre = "Pedro"          # Correcto

# 2edad = 20                Incorrecto
# nombre usuario = "Ana"   Incorrecto
```

### Asignación múltiple

```python
nombre, edad, ciudad = "Carlos", 20, "Madrid"

x = y = z = 10
```

### Actualización de variables

```python
contador = 5
contador = contador + 1

# Asignación abreviada
contador += 1
```

### Consultar el tipo de una variable

```python
nombre = "Carlos"

print(type(nombre))
```

`type()` devuelve el tipo de dato del objeto.

---

## 🔢 3. TIPOS DE DATOS

Python dispone de diferentes tipos de datos para representar información.

### 3.1. Tipos numéricos

| Tipo | Descripción | Ejemplo |
|---|---|---|
| `int` | Números enteros | `25` |
| `float` | Números decimales | `3.14` |
| `complex` | Números complejos | `2 + 3j` |

```python
edad = 20
precio = 15.99
numero_complejo = 2 + 3j
```

### 3.2. Tipo texto: `str`

Representa cadenas de caracteres.

```python
nombre = "Carlos"
mensaje = 'Hola, mundo'

texto = """Texto
de varias líneas"""
```

### Operaciones con cadenas

```python
nombre = "Carlos"

print(nombre.upper())      # MAYÚSCULAS
print(nombre.lower())      # minúsculas
print(nombre.capitalize()) # Primera letra en mayúscula
print(len(nombre))         # Longitud
print(nombre.replace("C", "K"))
```

### 3.3. Tipo booleano: `bool`

Representa valores lógicos.

```python
es_mayor = True
tiene_permiso = False
```

Solo admite dos valores:

- `True`
- `False`

### 3.4. Tipo nulo: `None`

Representa la ausencia de un valor.

```python
resultado = None
```

---

## 🔄 4. CONVERSIÓN DE TIPOS

La conversión permite transformar un dato de un tipo a otro.

| Función | Conversión |
|---|---|
| `int()` | Convierte a entero |
| `float()` | Convierte a decimal |
| `str()` | Convierte a texto |
| `bool()` | Convierte a booleano |
| `list()` | Convierte a lista |
| `tuple()` | Convierte a tupla |
| `set()` | Convierte a conjunto |

### Ejemplos

```python
numero = "25"

entero = int(numero)
decimal = float(numero)
texto = str(entero)

print(entero)
print(decimal)
print(texto)
```

### Conversión de entrada

```python
edad = int(input("Introduce tu edad: "))
altura = float(input("Introduce tu altura: "))
```

---

## ⚙️ 5. OPERADORES

Los operadores permiten realizar operaciones matemáticas, comparaciones y operaciones lógicas.

### 5.1. Operadores aritméticos

| Operador | Operación | Ejemplo |
|---|---|---|
| `+` | Suma | `5 + 3` |
| `-` | Resta | `5 - 3` |
| `*` | Multiplicación | `5 * 3` |
| `/` | División | `5 / 3` |
| `//` | División entera | `5 // 3` |
| `%` | Módulo | `5 % 3` |
| `**` | Potencia | `5 ** 3` |

### 5.2. Operadores de comparación

| Operador | Significado |
|---|---|
| `==` | Igual a |
| `!=` | Diferente de |
| `>` | Mayor que |
| `<` | Menor que |
| `>=` | Mayor o igual |
| `<=` | Menor o igual |

### 5.3. Operadores lógicos

| Operador | Función |
|---|---|
| `and` | Verdadero si ambas condiciones son verdaderas |
| `or` | Verdadero si al menos una condición es verdadera |
| `not` | Invierte el valor lógico |

```python
edad = 20

print(edad >= 18 and edad <= 30)
print(edad < 18 or edad > 65)
print(not edad == 20)
```

### 5.4. Operadores de asignación

```python
numero = 10

numero += 5
numero -= 2
numero *= 3
numero /= 2
numero //= 2
numero %= 3
numero **= 2
```

### 5.5. Operadores de pertenencia

```python
frutas = ["manzana", "pera", "uva"]

print("pera" in frutas)
print("naranja" not in frutas)
```

### 5.6. Operadores de identidad

```python
a = [1, 2, 3]
b = a
c = [1, 2, 3]

print(a is b)
print(a is c)
print(a == c)
```

`is` comprueba identidad de objeto; `==` compara igualdad de valores.

---

## ⌨️ 6. ENTRADA Y SALIDA DE DATOS

### 6.1. Entrada: `input()`

Permite recibir información del usuario.

```python
nombre = input("Introduce tu nombre: ")

print("Hola", nombre)
```

`input()` devuelve siempre una cadena de texto (`str`).

### 6.2. Salida: `print()`

Permite mostrar información.

```python
nombre = "Carlos"
edad = 20

print(nombre)
print(edad)
print("Nombre:", nombre, "Edad:", edad)
```

### 6.3. Formateo de cadenas: f-strings

```python
nombre = "Carlos"
edad = 20

print(f"Mi nombre es {nombre} y tengo {edad} años")
```

También se pueden incluir operaciones:

```python
a = 10
b = 5

print(f"Resultado: {a + b}")
```

---

## 🔀 7. ESTRUCTURAS CONDICIONALES

Permiten ejecutar diferentes bloques de código dependiendo de una condición.

### 7.1. `if`

Ejecuta un bloque si la condición es verdadera.

```python
edad = 20

if edad >= 18:
    print("Eres mayor de edad")
```

### 7.2. `if - else`

Permite ejecutar una alternativa cuando la condición no se cumple.

```python
edad = 16

if edad >= 18:
    print("Mayor de edad")
else:
    print("Menor de edad")
```

### 7.3. `if - elif - else`

Permite evaluar múltiples condiciones.

```python
nota = 8

if nota >= 9:
    print("Excelente")
elif nota >= 7:
    print("Notable")
elif nota >= 5:
    print("Aprobado")
else:
    print("Suspenso")
```

### 7.4. Condicionales anidados

```python
edad = 20
tiene_documento = True

if edad >= 18:
    if tiene_documento:
        print("Acceso permitido")
    else:
        print("Falta documentación")
else:
    print("Acceso denegado")
```

### 7.5. Operador condicional

```python
edad = 20

mensaje = "Mayor de edad" if edad >= 18 else "Menor de edad"

print(mensaje)
```

---

## 🔁 8. ESTRUCTURAS REPETITIVAS

Permiten ejecutar instrucciones varias veces.

### 8.1. Bucle `while`

Repite un bloque mientras una condición sea verdadera.

```python
contador = 1

while contador <= 5:
    print(contador)
    contador += 1
```

### 8.2. Bucle `for`

Permite recorrer elementos de una secuencia o colección.

```python
frutas = ["manzana", "pera", "uva"]

for fruta in frutas:
    print(fruta)
```

### 8.3. Función `range()`

Genera una secuencia de números.

```python
for numero in range(5):
    print(numero)
```

También permite establecer inicio, final y salto:

```python
range(inicio, fin, paso)

for numero in range(1, 10, 2):
    print(numero)
```

El valor final no se incluye.

### 8.4. `break`

Finaliza un bucle inmediatamente.

```python
for numero in range(10):
    if numero == 5:
        break

    print(numero)
```

### 8.5. `continue`

Salta a la siguiente iteración.

```python
for numero in range(5):
    if numero == 2:
        continue

    print(numero)
```

### 8.6. `pass`

Permite dejar un bloque vacío temporalmente.

```python
if True:
    pass
```

---

## 🗂️ 9. ESTRUCTURAS DE DATOS

Python proporciona diferentes estructuras para almacenar y organizar colecciones de datos.

### 9.1. Listas: `list`

Colección ordenada, modificable y que permite elementos duplicados.

```python
frutas = ["manzana", "pera", "uva"]

print(frutas[0])
print(frutas[-1])
```

**Modificar elementos:**

```python
frutas[0] = "naranja"
```

**Métodos principales:**

| Método | Función |
|---|---|
| `append()` | Agrega un elemento al final |
| `insert()` | Inserta en una posición |
| `extend()` | Agrega varios elementos |
| `remove()` | Elimina un elemento |
| `pop()` | Elimina y devuelve un elemento |
| `clear()` | Elimina todos los elementos |
| `sort()` | Ordena la lista |
| `reverse()` | Invierte el orden |
| `index()` | Devuelve la posición de un elemento |
| `count()` | Cuenta las apariciones |

```python
numeros = [5, 2, 8, 1]

numeros.append(10)
numeros.insert(1, 7)
numeros.remove(2)
numeros.sort()

print(numeros)
```

### 9.2. Tuplas: `tuple`

Colección ordenada e inmutable. Permite elementos duplicados.

```python
coordenadas = (10, 20, 30)

print(coordenadas[0])
print(len(coordenadas))
```

No se pueden modificar sus elementos después de crearla.

**Tupla de un solo elemento:**

```python
tupla = (10,)
```

### 9.3. Conjuntos: `set`

Colección sin posiciones indexadas, sin elementos duplicados y modificable.

```python
numeros = {1, 2, 3, 4, 4}

print(numeros)
```

**Métodos principales:**

| Método | Función |
|---|---|
| `add()` | Agrega un elemento |
| `remove()` | Elimina un elemento; genera error si no existe |
| `discard()` | Elimina un elemento sin generar error si no existe |
| `pop()` | Elimina y devuelve un elemento |
| `clear()` | Vacía el conjunto |
| `union()` | Unión de conjuntos |
| `intersection()` | Intersección |
| `difference()` | Diferencia |

```python
a = {1, 2, 3}
b = {3, 4, 5}

print(a.union(b))
print(a.intersection(b))
print(a.difference(b))
```

### 9.4. Diccionarios: `dict`

Colección de pares clave-valor.

```python
persona = {
    "nombre": "Carlos",
    "edad": 20,
    "ciudad": "Madrid"
}
```

**Acceder a los valores:**

```python
print(persona["nombre"])
print(persona.get("edad"))
```

**Modificar y agregar datos:**

```python
persona["edad"] = 21
persona["profesion"] = "Desarrollador"
```

**Métodos principales:**

| Método | Función |
|---|---|
| `get()` | Obtiene un valor |
| `keys()` | Devuelve las claves |
| `values()` | Devuelve los valores |
| `items()` | Devuelve pares clave-valor |
| `update()` | Actualiza el diccionario |
| `pop()` | Elimina una clave |
| `clear()` | Vacía el diccionario |

**Recorrer un diccionario:**

```python
for clave, valor in persona.items():
    print(clave, valor)
```

### 9.5. Resumen de estructuras de datos

| Estructura | Ordenada | Modificable | Duplicados |
|---|---|---|---|
| `list` | Sí | Sí | Sí |
| `tuple` | Sí | No | Sí |
| `set` | No | Sí | No |
| `dict` | Sí | Sí | Las claves no |

---

## 🧩 10. FUNCIONES

Una función es un bloque de código reutilizable que realiza una tarea determinada.

### 10.1. Declaración

```python
def saludar():
    print("Hola, mundo")

saludar()
```

### 10.2. Parámetros y argumentos

```python
def saludar(nombre):
    print(f"Hola, {nombre}")

saludar("Carlos")
```

- Parámetro: variable definida en la función.
- Argumento: valor enviado al llamar la función.

### 10.3. Retorno: `return`

Permite devolver un resultado.

```python
def sumar(a, b):
    return a + b

resultado = sumar(10, 5)

print(resultado)
```

### 10.4. Parámetros con valores predeterminados

```python
def saludar(nombre="Usuario"):
    print(f"Hola, {nombre}")

saludar()
saludar("Carlos")
```

### 10.5. Argumentos nombrados

```python
def presentar(nombre, edad):
    print(nombre, edad)

presentar(edad=20, nombre="Carlos")
```

### 10.6. Funciones lambda

Funciones pequeñas y anónimas.

```python
sumar = lambda a, b: a + b

print(sumar(5, 3))
```

### 10.7. Alcance de variables

- Local: existe dentro de una función.
- Global: definida fuera de las funciones.

```python
mensaje = "Global"

def ejemplo():
    local = "Local"
    print(mensaje)
    print(local)

ejemplo()
```

---

## ⚠️ 11. MANEJO DE EXCEPCIONES

Permite controlar errores que pueden producirse durante la ejecución.

### 11.1. `try - except`

```python
try:
    numero = int(input("Introduce un número: "))
    print(numero)

except ValueError:
    print("Debes introducir un número válido")
```

### 11.2. `else`

Se ejecuta cuando no ocurre una excepción.

```python
try:
    resultado = 10 / 2

except ZeroDivisionError:
    print("No se puede dividir entre cero")

else:
    print(resultado)
```

### 11.3. `finally`

Se ejecuta siempre, haya ocurrido una excepción o no.

```python
try:
    print("Ejecutando operación")

except Exception:
    print("Ha ocurrido un error")

finally:
    print("Proceso finalizado")
```

### 11.4. `raise`

Permite generar una excepción manualmente.

```python
edad = -5

if edad < 0:
    raise ValueError("La edad no puede ser negativa")
```

---

## ✅ 12. BUENAS PRÁCTICAS

- Utilizar nombres descriptivos para variables y funciones.
- Aplicar la convención `snake_case` para variables y funciones.
- Mantener una indentación de cuatro espacios.
- Evitar repetir código innecesariamente.
- Utilizar comentarios cuando aporten información útil.
- Dividir programas grandes en funciones.
- Validar los datos recibidos.
- Manejar las excepciones adecuadamente.
- Mantener el código legible y organizado.

### Ejemplo de código organizado

```python
def calcular_promedio(notas):
    if not notas:
        return None

    return sum(notas) / len(notas)


notas = [8, 9, 7, 10]

promedio = calcular_promedio(notas)

print(f"Promedio: {promedio}")
```

---

## 🚀 OBJETIVO DEL REPOSITORIO

Construir una base de conocimientos sobre Python mediante el estudio, la práctica y la documentación de sus fundamentos.

**Aprendiendo · Practicando · Construyendo**

