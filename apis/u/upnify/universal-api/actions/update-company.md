# Upnify: Update Company

Updates an existing company in Upnify.

```
PUT https://connect.mindcloud.co/v1/universal/upnify/latest/actions/update-company
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Upnify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/upnify/latest/actions/update-company" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "tkEmpresa": "string",
  "empresa": "string",
  "url": "https://example.com",
  "telefonoCorporativo": "string",
  "tkIndustria": "string",
  "direccion1": "string",
  "direccion2": "string",
  "ciudad": "string",
  "codigoPostal": "string",
  "idPais": "string",
  "idEstado": "string",
  "idMunicipio": "string",
  "numeroInterior": 1,
  "numeroExterior": 1,
  "tkCorporativo": "string",
  "idExterno": "string",
  "numeroEmpleados": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/upnify/latest/actions/update-company', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "tkEmpresa": "string",
    "empresa": "string",
    "url": "https://example.com",
    "telefonoCorporativo": "string",
    "tkIndustria": "string",
    "direccion1": "string",
    "direccion2": "string",
    "ciudad": "string",
    "codigoPostal": "string",
    "idPais": "string",
    "idEstado": "string",
    "idMunicipio": "string",
    "numeroInterior": 1,
    "numeroExterior": 1,
    "tkCorporativo": "string",
    "idExterno": "string",
    "numeroEmpleados": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `tkEmpresa` | string | yes | Código token que identifica de forma única a una empresa en el sistema, la cual se requiere modificar. ¿Dónde obtengo el token? |
| `empresa` | string | yes | Contiene el nombre de la empresa. |
| `url` | string | yes | Contiene la dirección de la página web de la empresa. |
| `telefonoCorporativo` | string | yes | Indica el número de teléfono de la nueva empresa (Si tiene un valor no númerico, devolvera un String). |
| `tkIndustria` | string | yes | Código token que identifica de forma única a una industria en el sistema. ¿Dónde obtengo el token? |
| `direccion1` | string | yes | Dirección que representa la ubicación de la empresa. |
| `direccion2` | string | yes | En caso de existir, se añade una segunda dirección. |
| `ciudad` | string | yes | Ciudad donde se encuentra establecida la empresa. |
| `codigoPostal` | string | yes | Código postal que pertenece a la zona de la empresa. |
| `idPais` | string | yes | Clave del país donde se encuentra establecida la empresa. ¿Dónde obtengo el id? |
| `idEstado` | string | yes | Clave del estado del país donde se encuentra establecida la empresa. ¿Dónde obtengo el id? |
| `idMunicipio` | string | yes | Clave del municipio del estado donde se encuentra establecida la empresa. ¿Dónde obtengo el id? |
| `numeroInterior` | number | yes | Variable que forma parte de la dirección de la empresa. |
| `numeroExterior` | number | yes | Variable que forma parte de la dirección de la empresa. |
| `tkCorporativo` | string | yes | Código token que identifica a un Grupo de compañia. |
| `idExterno` | string | yes | Identificador unico, no obligatorio para la interconexión con sistemas externos. |
| `numeroEmpleados` | number | yes | Contiene un número de empleados de la empresa. |

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

Through the native Upnify API, this operation is `PUT v4/empresas/:tkEmpresa` (base URL `https://api.upnify.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-company.md) for the provider-specific parameters and requirements.

