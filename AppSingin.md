## Iniciar sesión como aplicación

### Endpoints
* <span style="color:red">`http://190.60.234.203:8081/api`</span> (Desarrollo)
* <span style="color:red">`http://190.60.234.203:8081/api`</span> (Producción)

### Descripción
Provee la autenticación para las aplicaciones.

|URL|Method|Content-Type
|:-:|:-:|:-:
|/auth/app/signin|`POST`|application/x-www-form-urlencoded

### Query strings
`N/A`

### Header
|Llave|Tipo|Requerido|Descripción
|:-:|:-:|:-:|:-:|
|X-PRO-Auth-App|`String`|Si|Identificador de la aplicación
|X-PRO-Auth-Payload|`String`|Si|Conjunto de datos particulares para la solicitud.

#### Datos esperados en el Payload
|Llave|Tipo|Requerido|Descripción
|:-:|:-:|:-:|:-:|
|Nonce|`String`|Si|Identificador único para la solicitud.
|Epoch|`String`|Si|Hora de la solicitud en milisegundos.

#### Ejemplo
```javascript
{
    "X-PRO-Auth-App": "29b35be3-3159-4800-807e-cde138439378",
    "X-PRO-Auth-Payload": "eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJOb25jZSI6IjRhNTU1NDhkLWJiN2QtNDViMS1hOWQwLWM4ODcyZWFhMjA1ZSIsIlBhc3N3b3JkIjoiY29sb21iaWEiLCJEb2NUeXBlIjoiQ0MiLCJEZXZpY2VJZCI6IlBEUDAzOFxcZG1vbnRhbHZvIiwiRG9jTnVtYmVyIjoiMTIzNDU2In0.T_k_hOkp8h43hH5mFHMPgS0wPtZM929w3N273VjIM3E"
}
```

### Body
`N/A`

### Respuesta exitosa
```javascript
{
    Value1: 123,
    Value2: "Example"
}
```

### Respuesta de error
```javascript
{
    Value1: 123,
    Value2: "Example"
}
```

### Respuestas habituales del servidor
* **`200 (Ok)`** - La solicitud fue exitosa.

### Historial de Versiones

A continuación se muestra el historial de versiones de esta API:

|Versión|Fecha de lanzamiento|Descripción
|:-:|:-:|:-:|
|**1.0**|09/05/2018|Version inicial
