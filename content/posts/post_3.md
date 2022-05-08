---
title: "Agregando pruebas de unidad en tu proyecto JS"
date: 2022-05-08
description: 'Aca te contare como puedes agregar una dependencia llamada jest para realizar pruebas de unidad'
---
Para esta post debes tener un proyecto en JS, aprenderas una tecnica para diseñar tu app, estos conceptos podras trasladarlos a cualquier otro ámbito del software.
# Agregando las dependencias
Una vez teniendo un proyecto de JS:
>Si quieres ver como hacer un proyecto en JS visita mi post anterior.
<a href="https://dennisperez97.github.io/my_launchx_blog/posts/post_2/" target="_blank"><img src="https://img.shields.io/badge/Check%20Post-Creacion%20de%20proyecto%20JS-blue"></a>


1.Ejecuta `npm install --save-dev jest` para agregar jest
2.Modifica tu archivo `package.json`, para que al ejecutar el comando npm test se pueda ejecutar jest, agregaras en el apartado de `"scripts"` el siguiente comando.

Para linux
> "test": "node ./node_modules/.bin/jest"

Para windows

> "test": "node ./node_modules/jest/bin/jest"

3.Crea dos directorios `app` y `test`, crea en la raiz el archivo `index.js`

# Agregando una prueba de unidad vacia

4.En la carpeta test agrega una prueba de unidad en jest, procura que tenga el formato `ARCHIVOAPROBAR.test.js`, el archivo a probar puede ser cualquier modulo que tengas en tu proyecto, basta con referenciarlo dentro de la prueba y ejecutarlo como se utiliza en el proyecto.
Dentro del archivo pondras una prueba de unidad que lleva el siguiente formado:

>describe("Test Suite Description", () => {
  test('Case 1 Description', () => {
  ///Aca va todo tu script, para fines del post se utilizara la siguiente suma
    const resultOfSomething = 1 + 2
    expect(resultOfSomething).toBe(18);
  });
})
5. Verifica que esta prueba se ejecute, te recomiendo hacerla fallar para corroborar que se esta ejecutando bien, la ejecutas utilizando el comando `npm test test/ARCHIVOAPROBAR.test.js`
![image](https://user-images.githubusercontent.com/99489937/167312722-8f27f989-8a97-43dd-8dd9-8f1972d9bc47.png)

Como observas en la imagen, se ejecuto la prueba pero fallo pues se esperaba un valor de 18 (`.toBe(18)`) y se recibio un 3 ('1+2').

# Test Driven Development by Martin Fowler
>TDD Design Software Technique

1. Write a test for the next bit of functionality you want to add.
2. Write the functional code until the test passes.
3. Refactor both new and old code to make it well structured.

Referencia: TDD by Martin Fowler
