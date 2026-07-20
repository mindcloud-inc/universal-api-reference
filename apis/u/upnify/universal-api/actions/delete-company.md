# Upnify: Delete Company

Deletes an existing company from Upnify.

```
DELETE https://connect.mindcloud.co/v1/universal/upnify/latest/actions/delete-company
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Upnify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/upnify/latest/actions/delete-company?connectionId=$CONNECTION_ID&tkEmpresa=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "tkEmpresa": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/upnify/latest/actions/delete-company?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `tkEmpresa` | string | yes | Código token que identifica de forma única a una empresa en el sistema, la cual será eliminada. ¿Dónde obtengo el token? |

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

Through the native Upnify API, this operation is `DELETE v4/empresas/:tkEmpresa` (base URL `https://api.upnify.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-company.md) for the provider-specific parameters and requirements.

