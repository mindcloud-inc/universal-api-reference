# Upnify: Create Client

Creates a new client in Upnify.

```
POST https://connect.mindcloud.co/v1/universal/upnify/latest/actions/create-client
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Upnify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/upnify/latest/actions/create-client" \
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
const response = await fetch('https://connect.mindcloud.co/v1/universal/upnify/latest/actions/create-client', {
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
| `nombre` | string | yes | Contiene el nombre del nuevo cliente. |
| `tkEmpresa` | string | no | Código token que identifica de forma única a una empresa dentro el sistema, a la cuál pertenecerá el nuevo cliente. ¿Dónde obtengo el token? |
| `apellidos` | string | no | Almacena los apellidos del cliente. |
| `titulo` | string | no | Almacena el título del cliente. |
| `puesto` | string | no | Almacena el puesto que ocupa el cliente en la empresa. |
| `empresa` | string | yes | Almacena el nombre de la empresa a la que pertenece el cliente. |
| `correo` | string | no | Especifica el correo del cliente. |
| `noEmpleado` | number | no | Especifica el número de empleado del cliente en la empresa. |
| `calle` | string | no | Contiene el nombre o número de la calle, que forma parte de la ubicación del cliente. |
| `colonia` | string | no | Contiene el nombre o número de la colonia, que forma parte de la ubicación del cliente. |
| `telefono` | string | yes | Almacena el número de teléfono que pertenece al cliente (Si tiene un valor no númerico, devolvera un String). |
| `telefono2` | string | no | En caso de existir, se guarda un número de teléfono secundario del cliente (Si tiene un valor no númerico, devolvera un String). |
| `movil` | string | no | Almacena un número de teléfono movil del cliente (Si tiene un valor no númerico, devolvera un String). |
| `idPais` | string | no | Código que indica el país del nuevo cliente. ¿Donde obtengo el Id? |
| `idEstado` | string | no | Código que indica un estado del país. ¿Donde obtengo el Id? |
| `idMunicipio` | string | no | contiene un código que indica un municipio de un estado. ¿Donde obtengo el Id? |
| `ciudad` | string | no | Contiene la ciudad del cliente. |
| `codigoPostal` | string | no | Indica el código postal del nuevo cliente. |
| `tkFase` | string | no | Código token que identifica de forma única a una fase dentro el sistema. ¿Donde obtengo el Token? |
| `tkOrigen` | string | no | Código token que identifica de forma única a una fase dentro el sistema. ¿Donde obtengo el Token? |
| `sexo` | string | no | Indica el sexo del nuevo cliente. - H Hombre. - M Mujer. |
| `url` | string | no | Contiene la url del sitio web del cliente. |
| `facebook` | string | no | Contiene la url del sitio de facebook del cliente. |
| `twitter` | string | no | Contiene la url del sitio de twitter del cliente. |
| `skype` | string | no | Contiene la url del sitio de skype del cliente. |
| `linkedin` | string | no | Contiene la url del sitio de linkedin del cliente. |
| `googlePlus` | string | no | Contiene la url del sitio de googlePlus del cliente. |
| `comentarios` | string | no | Contiene un comentario para el nuevo cliente. |
| `cp1` | string | no | Contiene el valor del primer campo personalizado, se pueden colocar hasta 100 y son definidos por el usuario. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": 1,
      "details": [
        {}
      ],
      "msg": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | number | Response status code returned by Upnify when creating a client. |
| `details` | array<object> | Additional result details, including the token of the created client when available. |
| `msg` | string | Human-readable result message returned by Upnify. |

## Native endpoint

Through the native Upnify API, this operation is `POST v4/clientes` (base URL `https://api.upnify.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-client.md) for the provider-specific parameters and requirements.

