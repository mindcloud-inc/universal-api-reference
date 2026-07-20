# Upnify: Create Prospect

Creates a new prospect in Upnify.

```
POST https://connect.mindcloud.co/v1/universal/upnify/latest/actions/create-prospect
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Upnify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/upnify/latest/actions/create-prospect" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "nombre": "string",
  "empresa": "string",
  "telefono": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/upnify/latest/actions/create-prospect', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "nombre": "string",
    "empresa": "string",
    "telefono": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `nombre` | string | yes | Contiene el nombre del nuevo prospecto. |
| `tkEmpresa` | string | no | Código token que identifica de forma única a una empresa dentro el sistema, a la cuál pertenecerá el nuevo prospecto. ¿Dónde obtengo el token? |
| `apellidos` | string | no | Almacena los apellidos del prospecto. |
| `titulo` | string | no | Almacena el título del prospecto. |
| `puesto` | string | no | Almacena el puesto que ocupa el prospecto en la empresa. |
| `empresa` | string | yes | Almacena el nombre de la empresa a la que pertenece el prospecto. |
| `correo` | string | no | Especifica el correo del prospecto. |
| `noEmpleado` | number | no | Especifica el número de empleado del prospecto en la empresa. |
| `calle` | string | no | Contiene el nombre o número de la calle, que forma parte de la ubicación del prospecto. |
| `colonia` | string | no | Contiene el nombre o número de la colonia, que forma parte de la ubicación del prospecto. |
| `telefono` | string | yes | Almacena el número de teléfono que pertenece al prospecto (Si tiene un valor no númerico, devolvera un String). |
| `telefono2` | string | no | En caso de existir, se guarda un número de teléfono secundario del prospecto (Si tiene un valor no númerico, devolvera un String). |
| `movil` | string | no | Almacena un número de teléfono movil del prospecto (Si tiene un valor no númerico, devolvera un String). |
| `idPais` | string | no | Código que indica el país del nuevo prospecto. ¿Donde obtengo el Id? |
| `idEstado` | string | no | Código que indica un estado del país. ¿Donde obtengo el Id? |
| `idMunicipio` | string | no | contiene un código que indica un municipio de un estado. ¿Donde obtengo el Id? |
| `ciudad` | string | no | Contiene la ciudad del prospecto. |
| `codigoPostal` | string | no | Indica el código postal del nuevo prospecto. |
| `tkFase` | string | no | Código token que identifica de forma única a una fase dentro el sistema. ¿Donde obtengo el Token? |
| `tkOrigen` | string | no | Código token que identifica de forma única a una fase dentro el sistema. ¿Donde obtengo el Token? |
| `sexo` | string | no | Indica el sexo del nuevo prospecto. - H Hombre. - M Mujer. |
| `url` | string | no | Contiene la url del sitio web del prospecto. |
| `facebook` | string | no | Contiene la url del sitio de facebook del prospecto. |
| `twitter` | string | no | Contiene la url del sitio de twitter del prospecto. |
| `skype` | string | no | Contiene la url del sitio de skype del prospecto. |
| `linkedin` | string | no | Contiene la url del sitio de linkedin del prospecto. |
| `googlePlus` | string | no | Contiene la url del sitio de googlePlus del prospecto. |
| `comentarios` | string | no | Contiene un comentario para el nuevo prospecto. |
| `cp1` | string | no | Contiene el valor del primer campo personalizado, se pueden colocar hasta 100 y son definidos por el usuario. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": 1,
      "details": "string",
      "msg": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | number | Proporciona un código de verificación como respuesta.  - 0 Proceso correcto. - 1 Falló la inserción. - 2 Faltan parámetros. - 3 Error al eliminar el registro. - 4 Token de sesión vencido.  - 5 Fallo de procedimiento en base de datos. - 6 Permisos insuficientes. - 7 Mensajes en la lógica de negocios. |
| `details` | string | Contiene el token del nuevo registro creado, el nombre de la variable "tkNombreVariable", deberá coincidir con el nombre de la variable que contiene el token del nuevo registro agregado. |
| `msg` | string | Proporciona un mensaje descriptivo o razón dependiendo el resultado. |

## Native endpoint

Through the native Upnify API, this operation is `POST v4/prospectos` (base URL `https://api.upnify.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-prospect.md) for the provider-specific parameters and requirements.

