# LLM from Scratch (Karpathy Zero to Hero Series)

Implementación educativa de un modelo de lenguaje desde cero, siguiendo la serie **Neural Networks: Zero to Hero** de **Andrej Karpathy**.

El objetivo de este proyecto es entender cómo funcionan los modelos de lenguaje **desde primeros principios**, comenzando con texto sin procesar y construyendo progresivamente los componentes necesarios para entrenar un modelo de lenguaje.

Este repositorio prioriza **comprender los fundamentos antes que usar librerías de alto nivel**.

---

# Objetivos del proyecto

Este proyecto busca:

- comprender cómo funcionan los modelos de lenguaje internamente
- implementar los bloques fundamentales de un LLM
- aprender tokenización y construcción de vocabulario
- entender cómo el texto se convierte en números
- seguir paso a paso la metodología de la serie de Karpathy

El enfoque es **aprender implementando**.

---

# Contenido actual

## 1. Preprocesamiento de texto

Se trabaja con texto sin procesar para:

- leer el dataset
- limpiar el texto
- separar palabras y signos de puntuación
- tokenizar usando expresiones regulares

Ejemplo de texto original:

```
Hello, world. This is a test.
```

Se convierte en tokens:

```
["Hello", ",", "world", ".", "This", "is", "a", "test"]
```

---

## 2. Construcción del vocabulario

A partir de los tokens se construye un vocabulario que permite convertir texto en números.

Se generan dos diccionarios fundamentales:

- `token → índice`
- `índice → token`

Ejemplo:

```
{
"Hello": 0,
",": 1,
"world": 2,
".": 3
}
```

Esto permite representar texto de forma numérica para que pueda ser procesado por un modelo.

---

## 3. Implementación de un tokenizador simple

Se implementa una clase mínima de tokenización.

Ejemplo de uso:

```python
tokenizer = SimpleTokenizerV1(vocab)

encoded = tokenizer.encode("Hello world")
decoded = tokenizer.decode(encoded)
```

Donde:

- `encode()` convierte texto en una secuencia de enteros
- `decode()` convierte los enteros nuevamente en texto

---

# Estructura del proyecto

```
llm-from-scratch-karpathy/

│
├── llm_from_scratch.ipynb
│   Notebook principal con la implementación paso a paso
│
├── the-verdict.txt
│   Dataset de texto utilizado para los experimentos
│
└── README.md
```

---

# Conceptos que se aprenden

Este proyecto introduce conceptos fundamentales para comprender los LLM:

- tokenización
- vocabulario
- codificación de texto
- preprocesamiento de datos
- representación numérica del lenguaje

En etapas posteriores, este tipo de proyecto suele evolucionar hacia:

- modelos a nivel de carácter
- modelos bigram
- redes neuronales simples
- transformers

---

# Referencia

Serie original:

**Andrej Karpathy – Neural Networks: Zero to Hero**

YouTube:

https://www.youtube.com/@AndrejKarpathy

---

# ¿Por qué construir un LLM desde cero?

Las librerías modernas abstraen gran parte de la complejidad.

Construir los componentes manualmente permite entender:

- qué es realmente un token
- cómo el texto se transforma en números
- cómo los modelos aprenden patrones estadísticos del lenguaje

Comprender estos fundamentos es clave para trabajar con:

- LLMs
- NLP
- Ingeniería de IA
