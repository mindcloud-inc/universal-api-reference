# Upnify: Update Client

Updates an existing client in Upnify.

```
PUT https://connect.mindcloud.co/v1/universal/upnify/latest/actions/update-client
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Upnify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/upnify/latest/actions/update-client" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "tkCliente": "string",
  "aprobacionEstado": 1,
  "esCanalizado": 1,
  "tkEmpresa": "string",
  "descartado": 1,
  "etiquetarSeguimiento": 1,
  "compartirReasignar": 1,
  "oportunidadArchivar": 1,
  "descartar": 1,
  "aprobar": 1,
  "rechazar": 1,
  "compartido": "string",
  "emailConfigurado": "ava@example.com",
  "esDescartado": 1,
  "nombreCliente": "string",
  "nombre": "string",
  "apellidos": "string",
  "puesto": "string",
  "empresa": "string",
  "correo": "string",
  "telefono1": "string",
  "telefono2": "string",
  "movil": "string",
  "idPais": "string",
  "idEstado": "string",
  "ciudad": "string",
  "idMunicipio": "string",
  "tkFase": "string",
  "origen": "string",
  "proximoEvento": "string",
  "cp1": 1,
  "pCat1": "string",
  "eCat1": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/upnify/latest/actions/update-client', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "tkCliente": "string",
    "aprobacionEstado": 1,
    "esCanalizado": 1,
    "tkEmpresa": "string",
    "descartado": 1,
    "etiquetarSeguimiento": 1,
    "compartirReasignar": 1,
    "oportunidadArchivar": 1,
    "descartar": 1,
    "aprobar": 1,
    "rechazar": 1,
    "compartido": "string",
    "emailConfigurado": "ava@example.com",
    "esDescartado": 1,
    "nombreCliente": "string",
    "nombre": "string",
    "apellidos": "string",
    "puesto": "string",
    "empresa": "string",
    "correo": "string",
    "telefono1": "string",
    "telefono2": "string",
    "movil": "string",
    "idPais": "string",
    "idEstado": "string",
    "ciudad": "string",
    "idMunicipio": "string",
    "tkFase": "string",
    "origen": "string",
    "proximoEvento": "string",
    "cp1": 1,
    "pCat1": "string",
    "eCat1": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `tkCliente` | string | yes | El código token que identifica a un cliente de manera única dentro del CRM, al cual se requiere modificar su información. ¿Dónde obtengo el token? |
| `aprobacionEstado` | number | yes | Código que indica si el cliente necesita ser aprobado por el dueño de la compañia con la cual se registró el prospecto. - 0 No requiere aprobación. - 1 Se reuiere aprobación. </ul |
| `esCanalizado` | number | yes | Código que indica si el registro es canalizado o no. |
| `tkEmpresa` | string | yes | Código token que identifica de forma única a una empresa dentro el sistema. ¿Dónde obtengo el token? |
| `descartado` | number | yes | Código que indica si el cliente se encuentra descartado. - 0 Cliente no descartado. - 1 Cliente descartado. |
| `etiquetarSeguimiento` | number | yes | Se indica si el ejecutivo puede agregar seguimientos al cliente. |
| `compartirReasignar` | number | yes | Se indica si el ejecutivo puede reasignar a un cliente. |
| `oportunidadArchivar` | number | yes | Se indica si el ejecutivo puede archivar a un cliente. |
| `descartar` | number | yes | Se indica si el ejecutivo puede descartar a un cliente. |
| `aprobar` | number | yes | Se indica si el ejecutivo puede dar la aprobación a un cliente. |
| `rechazar` | number | yes | Se indica si el ejecutivo puede rechazar un cliente. |
| `compartido` | string | yes | Indica si el cliente se encuentra actualmente compartido. |
| `emailConfigurado` | string | yes | Indica si la cuenta del ejecutivo tiene la configuración de email. |
| `esDescartado` | number | yes | Contiene un código que define si el cliente es descartado o no. - 0 Cliente no descartado. - 1 Cliente descartado. |
| `nombreCliente` | string | yes | Guarda el nombre del cliente. |
| `nombre` | string | yes | Contiene el nombre del cliente. |
| `apellidos` | string | yes | Almacena los apellidos del cliente. |
| `puesto` | string | yes | Almacena el puesto que ocupa el cliente en la empresa. |
| `empresa` | string | yes | Guarda el nombre de la empresa a la que pertenece el cliente. |
| `correo` | string | yes | Especifica el correo del cliente. |
| `telefono1` | string | yes | Almacena el número de teléfono que pertenece al cliente (Si tiene un valor no númerico, devolvera un String). |
| `telefono2` | string | yes | En caso de existir, se guarda un número de teléfono secundario del cliente (Si tiene un valor no númerico, devolvera un String). |
| `movil` | string | yes | Almacena un número de teléfono movil del cliente (Si tiene un valor no númerico, devolvera un String). |
| `idPais` | string | yes | Código que indica el país del nuevo prospecto. ¿Dónde obtengo el id? |
| `idEstado` | string | yes | Código que indica un estado del país. ¿Dónde obtengo el id? |
| `ciudad` | string | yes | Contiene la ciudad del prospecto. |
| `idMunicipio` | string | yes | contiene un código que indica un municipio de un estado. ¿Dónde obtengo el id? |
| `tkFase` | string | yes | Código token que identifica de forma única a una fase dentro el sistema. ¿Dónde obtengo el token? |
| `origen` | string | yes | Guarda el origen desde la cual se originó una oportunidad. |
| `proximoEvento` | string | yes | Contiene un arrelgo de datos que proporciona los datos de un evento. |
| `cp1` | number | yes | Contiene el nombre del primer campo personalizado, se pueden colocar hasta 100. |
| `pCat1` | string | yes | Primer catálogo personalizado, contiene el id del valor seleccionado de los catálogos adicionales para clientes, los cuales son elegidos por el usuario. |
| `eCat1` | string | yes | Primer catálogo personalizado, contiene el id del valor seleccionado de los catálogos adicionales para empresas, los cuales son elegidos por el usuario |

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
| `code` | number | Proporciona un código de verificación como respuesta. |
| `msg` | string | Proporciona un mensaje descriptivo o razón dependiendo el resultado.  - 0 Proceso correcto. - 1 Falló la inserción. - 2 Faltan parámetros. - 3 Error al eliminar el registro. - 4 Token de sesión vencido.  - 5 Fallo de procedimiento en base de datos. - 6 Permisos insuficientes. - 7 Mensajes en la lógica de negocios. |

## Native endpoint

Through the native Upnify API, this operation is `PUT v4/clientes/:tkCliente` (base URL `https://api.upnify.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-client.md) for the provider-specific parameters and requirements.

