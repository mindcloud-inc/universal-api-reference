# Upnify: Create Company

Creates a new company in Upnify.

```
POST https://connect.mindcloud.co/v1/universal/upnify/latest/actions/create-company
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Upnify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/upnify/latest/actions/create-company" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "empresa": "string",
  "tkIndustria": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/upnify/latest/actions/create-company', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "empresa": "string",
    "tkIndustria": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `empresa` | string | yes | Contiene el nombre de la empresa. |
| `tkIndustria` | string | yes | Código token que identifica de forma única a una industria en el sistema. ¿Dónde obtengo el token? |
| `url` | string | no | Contiene la dirección de la página web de la empresa. |
| `telefonoCorporativo` | string | no | Indica el número de teléfono de la nueva empresa (Si tiene un valor no númerico, devolvera un String). |
| `direccion1` | string | no | Dirección que representa la ubicación de la empresa. |
| `direccion2` | string | no | En caso de existir, se añade una segunda dirección. |
| `ciudad` | string | no | Ciudad donde se encuentra establecida la empresa. |
| `codigoPostal` | string | no | Código postal que pertenece a la zona de la empresa. |
| `idPais` | string | no | Clave del país donde se encuentra establecida la empresa. ¿Dónde obtengo el id? |
| `idEstado` | string | no | Clave del estado del país donde se encuentra establecida la empresa. ¿Dónde obtengo el id? |
| `idMunicipio` | string | no | Clave del municipio del estado donde se encuentra establecida la empresa. ¿Dónde obtengo el id? |
| `numeroInterior` | number | no | Variable que forma parte de la dirección de la empresa. |
| `numeroExterior` | number | no | Variable que forma parte de la dirección de la empresa. |
| `tkCorporativo` | string | no | Código token que identifica a un Grupo de compañia. |
| `idExterno` | string | no | Identificador unico, no obligatorio para la interconexión con sistemas externos. |
| `numeroEmpleados` | number | no | Contiene un número de empleados de la empresa. |

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
| `details` | string | Contiene el token del nuevo registro creado, el nombre de la variable "tkEmpresa", deberá coincidir con el nombre de la variable que contiene el token del nuevo registro agregado. |
| `msg` | string | Proporciona un mensaje descriptivo o razón dependiendo el resultado. |

## Native endpoint

Through the native Upnify API, this operation is `POST v4/empresas` (base URL `https://api.upnify.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-company.md) for the provider-specific parameters and requirements.

