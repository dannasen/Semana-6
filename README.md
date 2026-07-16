semana 6

touch preguntas-semana6.txt 


*2. http://preguntas-semana6.txt*
Pregunta 1:
Respuesta: B. Un formato de intercambio de datos usado entre aplicaciones

Pregunta 2:
Respuesta: B. Leer datos enviados en formato JSON en una petición

Pregunta 3:
Respuesta: B. req.body

Pregunta 4:
Respuesta: C. { "nombre": "Juan" }
---

*3. http://server.js* 
const express = require('express');
const app = express();

app.use(express.json());

app.post('/registro', (req, res) => {
    const nombre = req.body.nombre;
    const mensaje = req.body.mensaje;

    res.json({
        estado: "Datos recibidos",
        nombre: nombre,
        mensaje: mensaje
    });
});

app.listen(3000, () => {
    console.log('Servidor ejecutándose en puerto 3000');
});
---

*4. http://prueba-api.txt*
Prueba de la ruta POST /registro

URL: http://localhost:3000/registro
Método: POST
JSON enviado:
{
  "nombre": "Maria",
  "mensaje": "Hola comunidad"
}

Respuesta del servidor:
{
  "estado": "Datos recibidos",
  "nombre": "Maria",
  "mensaje": "Hola comunidad"
}
