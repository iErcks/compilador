# Compilador en Python (Proyecto ESCOM)

Este proyecto es un **compilador educativo** implementado en Python usando Jupyter Notebook. Fue desarrollado como parte de la materia de Compiladores en la Escuela Superior de Cómputo (ESCOM-IPN). El compilador permite analizar y **ejecutar código fuente** simulado (inspirado en lenguajes como C) mediante fases clásicas de compilación.

---

## Características del proyecto

- ✅ Análisis léxico con expresiones regulares
- ✅ Análisis sintáctico predictivo
- ✅ Evaluación de expresiones aritméticas
- ✅ Tabla de símbolos para variables
- ✅ Comentarios técnicos para cada función
- ✅ Notebook interactivo y educativo

---

## Estructura del repositorio

Compilador/
├── notebook/
│ └── compilador.ipynb # Código principal del compilador en Jupyter
├── ejemplos/ 
│ └── codigo.txt  #Codigo a ejecutar. Aqui debes programar :)
├── README.md # Descripción del proyecto
├── LICENSE # Licencia de uso (MIT)
└── .gitignore


## ⚙️ ¿Cómo funciona el compilador?

Este compilador educativo soporta una serie de construcciones fundamentales presentes en lenguajes de programación como C y VHL. Permite la **declaración de variables (enteras y flotantes)**, **definición de funciones no retornables**, **operaciones aritméticas**, **recursividad**, **estructuras condicionales**, **ciclos `for`**, e **impresión de variables**.

> 📌 **Importante:** La sintaxis del lenguaje es sencilla y requiere que **cada elemento esté separado por espacios**.

---

### 🧱 Estructura general del programa

El programa se divide en tres secciones:

1. **Declaración de variables**
2. **Definición de funciones**
3. **Bloque `main`**

#### 🔸 Declaración de variables

Las variables se declaran al inicio del programa con el bloque `declaration isBegin`.

```txt
declaration isBegin
    int cont ;
    int sum ;
    float dec ;
end
```

---

#### 🔸 Definición de funciones

Las funciones se definen usando la palabra clave `function` seguida del nombre de la función. No retornan valores, pero permiten reutilización de lógica.

```txt
function ASIGNA isBegin
    cont = 2 ;
    sum = 0 ;
end
```

---

#### 🔸 Bloque principal (`main`)

El código principal a compilar y ejecutar se encuentra dentro del bloque `main isBegin`.

```txt
main isBegin
    cont = 0 ;
    sum = 0 ;
    IMPRIMIR () ;
end
```

---

### ➕ Operaciones aritméticas

Se permiten operaciones básicas con paréntesis:

```txt
dec = ( 10 + 1 ) / 2 ;
```

---

### 🔁 Estructuras de control

#### 🔹 Condicionales

Solo se admiten comparaciones con los operadores `<` y `>`.

```txt
if sum < 5 then
    sum = sum + 1 ;
end
```

#### 🔹 Ciclos `for`

Se admite una forma simplificada del ciclo `for`, con incremento de uno en uno.

```txt
for 1 : 6 then
    sum = sum + cont ;
    cont = cont + 1 ;
end
```

---

### 🧠 Llamada a funciones y recursividad

Es posible invocar funciones desde otras funciones o desde el `main`, lo que habilita el uso de **funciones anidadas y recursividad**.

```txt
main isBegin
    IMPRIMIR () ;
end
```

---

### 🧮 Implementación del compilador

El compilador se basa en el uso de **una pila de ejecución**, lo que permite soportar:

- Condiciones anidadas
- Ciclos anidados
- Llamadas recursivas

---

### 📁 Casos de prueba

En la carpeta `ejemplos/` encontrarás un archivo de entrada con código listo para ser probado. Puedes modificarlo para experimentar con nuevas instrucciones y comprender el comportamiento del compilador.
