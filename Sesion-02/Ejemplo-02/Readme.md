# EJEMPLO 2. Características de los objetos (`str`, `summary`, `head` y `View`)

#### Objetivo

- Conocer mejor conjuntos de datos guardados como data frames en `R` de una forma rápida, mediante algunas funciones útiles y de uso común.

#### Requisitos

- Haber instalado previamente R y RStudio 
- Saber interpretar las medidas de tendencia central y de posición

#### Desarrollo

#### Función `str`

`str` es una función que muestra de manera compacta la estructura interna de un objeto de `R`. Por ejemplo, si usamos como argumento de `str` el conjunto de datos `iris` que podemos encontrar en `R`

```R
str(iris)
```

entonces la salida de la instrucción nos muestra el tipo de objeto, número de observaciones y de variables, así como el tipo de dato al que corresponde cada variable.

#### Función `summary`

La función `summary` es una función genérica usada para obtener resumenes de diferentes objetos de `R`, por ejemplo

```R
summary(1:100)
summary(mtcars)
```

También es útil para obtener resumenes de los resultados de diferentes ajustes a modelos

```R
set.seed(57)
x <- rnorm(35)
e <- rnorm(35)
y <- 5 + 2*x + e
modelo <- lm(y~x)
summary(modelo)
```

#### Función `head`

La función `head` devuelve la primera parte de un data frame, tabla, matriz, vector o función. Por ejemplo, al usar el data frame `mtcars` como argumento de la función `head`, se devolverán únicamente las primeras seis filas del data frame

```R
head(mtcars)
```

la función `tail` funciona de manera similar, pero en lugar de devolver la primera parte de un objeto, devuelve la última parte de este, por ejemplo, al ejecutarse la siguiente instrucción

```R
tail(mtcars)
```

se devolverán las últimas seis filas del data frame

#### Función `View`

La función `View` aplicada a un objeto de `R` como un data frame, invoca un visor de datos al estilo de una hoja de cálculo, por ejemplo

```R
View(iris)
```
