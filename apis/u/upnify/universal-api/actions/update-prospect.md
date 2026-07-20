# Upnify: Update Prospect

Updates an existing prospect in Upnify.

```
PUT https://connect.mindcloud.co/v1/universal/upnify/latest/actions/update-prospect
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Upnify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/upnify/latest/actions/update-prospect" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "tkProspecto": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/upnify/latest/actions/update-prospect', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "tkProspecto": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `tkProspecto` | string | yes | El código token que identifica a un prospecto, al cual se requiere modificar su información. ¿Dónde obtengo el token? |
| `aprobacionEstado` | number | no | Contiene un código que define el estado de una aprobación realizada por el usuario. |
| `esCanalizado` | number | no | Almacena un código que define si el registro se encuentra canalizado o compartido. - 0 Registro no canalizado. - 1 Registro original o maestro. - 2 Registro esclavo. |
| `tkEmpresa` | string | no | Código token que identifica de forma única a una empresa dentro el sistema. ¿Dónde obtengo el token? |
| `descartado` | number | no | Código que indica si el prospecto se encuentra descartado. - 0 No está descartado. - 1 Prospecto descartado. |
| `nombre` | string | no | Contiene el nombre del prospecto. |
| `apellidos` | string | no | Almacena los apellidos del prospecto. |
| `puesto` | string | no | Almacena el puesto que ocupa el prospecto en la empresa. |
| `correo` | string | no | Especifica el correo del prospecto. |
| `telefono1` | string | no | Almacena el número de teléfono que pertenece al prospecto (Si tiene un valor no númerico, devolvera un String). |
| `telefono2` | string | no | En caso de existir, se guarda un número de teléfono secundario del prospecto (Si tiene un valor no númerico, devolvera un String). |
| `movil` | string | no | Almacena un número de teléfono movil del prospecto (Si tiene un valor no númerico, devolvera un String). |
| `tkFase` | string | no | Codigo token que identifica de forma única a una fase dentro el sistema. ¿Dónde obtengo el token? |
| `sexo` | string | no | Indica el sexo del nuevo prospecto. |
| `url` | string | no | Contiene la url del sitio web del prospecto. |
| `facebook` | string | no | Contiene la url del sitio de facebook del prospecto. |
| `twitter` | string | no | Contiene la url del sitio de twitter del prospecto. |
| `skype` | string | no | Contiene la url del sitio de skype del prospecto. |
| `linkedin` | string | no | Contiene la url del sitio de linkedin del prospecto. |
| `googlePlus` | string | no | Contiene la url del sitio de googlePlus del prospecto. |
| `cp1` | string | no | Contiene el valor del primer campo personalizado, se pueden colocar hasta 100 y son definidos por el usuario. |
| `tkOrigen` | string | no | Guarda el origen desde la cual se originó una oportunidad. ¿Donde obtengo el Token? |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": 1,
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
| `msg` | string | Proporciona un mensaje descriptivo o razón dependiendo el resultado. |

## Native endpoint

Through the native Upnify API, this operation is `PUT v4/prospectos/:tkProspecto` (base URL `https://api.upnify.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-prospect.md) for the provider-specific parameters and requirements.

