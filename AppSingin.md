## Iniciar sesión como aplicación

### Endpoints
* <span style="color:red">`http://localhost/api`</span> 
* <span style="color:red">`http://localhost/api`</span> 

### Descripción
Provee la autenticación para las aplicaciones.

|URL|Method|Content-Type
|:-:|:-:|:-:
|/auth/app/signin|`POST`|application/x-www-form-urlencoded

### Parámetros de URL
`N/A`

[comment]: Información cuando si tenga parámetros.
#### Segmentos de la URL
`/auth/app/signin/{Value1}/{Value2}`

#### Descripción
|Llave|Tipo|Requerido|Defecto|Descripción
|:-:|:-:|:-:|:-:|:-:|
|Value1|`String`|Si|``|Des
|Value2|`String`|Si|`Example`|Valor de ejemplo

#### Ejemplo
`/auth/app/signin/123/Example`

### Header
|Llave|Tipo|Requerido|Descripción
|:-:|:-:|:-:|:-:|
|X-PRO-Auth-App|`String`|Si|Identificador de la aplicación
|X-PRO-Auth-Payload|`String`|No|Conjunto de datos particulares para la solicitud.

#### Datos pata el Payload
|Llave|Tipo|Requerido|Descripción
|:-:|:-:|:-:|:-:|
|Nonce|`String`|Si|Identificador único para la solicitud.
|Epoch|`String`|Si|Hora de la solicitud en milisegundos.

[comment]: Cómo se indica aqui el maneja del JWT??

#### Ejemplo
```javascript
{
    "X-PRO-Auth-App": "29b35be3-3159-4800-807e-cde138439378",
    "X-PRO-Auth-Payload": "eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJOb25jZSI6IjRhNTU1NDhkLWJiN2QtNDViMS1hOWQwLWM4ODcyZWFhMjA1ZSIsIlBhc3N3b3JkIjoiY29sb21iaWEiLCJEb2NUeXBlIjoiQ0MiLCJEZXZpY2VJZCI6IlBEUDAzOFxcZG1vbnRhbHZvIiwiRG9jTnVtYmVyIjoiMTIzNDU2In0.T_k_hOkp8h43hH5mFHMPgS0wPtZM929w3N273VjIM3E"
}
```

### Body
`N/A`

[comment]: Información cuando si se espere un body.

|Llave|Tipo|Requerido|Defecto|Descripción
|:-:|:-:|:-:|:-:|:-:|
|Value1|`Integer`|Si|`123`|Valor de ejemplo
|Value2|`String`|No|`Example`|Valor de ejmplo

#### Ejemplo
```javascript
{
    Value1: 123,
    Value2: "Example"
}
```

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
