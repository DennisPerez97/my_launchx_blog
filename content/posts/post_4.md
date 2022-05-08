---
title: "Mi primer server con Express.js"
date: 2022-05-08
description: 'Aca veras como instalar e inicializar un server con express en JS'
---


# Creando mi primer server

1.Instala la dependencia en express con `npm install express --save
2. Crea un archivo llamado `app.js` y crea tu primera app de express.
3. Tenemos que configurar express e indicarle el puerto en el que se ejecutara
```js
// Usando objeto express
const express = require('express')
// App de Express
const app = express()
app.use(express.json()) // Indicamos que usaremos JSON
// Puerto en que vamos a ver nuestra app: localhost:3000
const port = 3000
// Con esto inicializamos esta app
app.listen(port, () => {
 console.log(`Example app listening on port ${port}`)
})
```
# Agrega los endpoint que desees

4. Utilizaremos el metodo GET de express para hacer un endpost, tendran el siguente formato

```
app.get('/turuta', (req,res) => {
//El codigo que necesites para generar las respuestas
    res.send("Hola este es la respuesta de /turuta") ///devuelves en un formato JSON
})


5. Levantas tu server con `node app.js`

# Endpint GET con Query params
Para fines del post realizaremos un codigo pequeño.
6. Agrega el siguiente codigo
![image](https://user-images.githubusercontent.com/99489937/167313484-cc764554-b021-4ab2-8493-8b3e4a6e22b6.png)

7. Levanta el servidor con `node app.js` y accede al url `localhost:3000/v1/explorers/:id` y reemplaza el :id por 1 para que te devuelva el explorer Carlos

# POST Crea un endpoint que se encargue de crear un explorer 

1. Agrega el siguiente código:

![image](https://user-images.githubusercontent.com/17634377/163704695-c4c3c9dc-4922-4db1-acc1-f550562bafb6.png)

2. Nota que el `status code` es 201.
3. Prueba el request 3 de postman.

# PUT Crea un endpoint que se encargue de actualizar un explorer

1. Agrega el siguiente código:

![image](https://user-images.githubusercontent.com/17634377/163704739-d2d44eff-499f-46be-bc8f-4ddcc4d3abbb.png)

2. Prueba el request 4 de postman.

# DELETE Crea un endpoint para eliminar un explorer

1. Agrega el siguiente código:

![image](https://user-images.githubusercontent.com/17634377/163704760-fa8d67d4-bd16-489e-940e-dd5703b3eafa.png)

2. Prueba el request 5 de postman.

Creditos a Carlos Gilmar de Inovaccion
