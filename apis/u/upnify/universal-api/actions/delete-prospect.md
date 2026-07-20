# Upnify: Delete Prospect

Deletes an existing prospect from Upnify.

```
DELETE https://connect.mindcloud.co/v1/universal/upnify/latest/actions/delete-prospect
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Upnify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/upnify/latest/actions/delete-prospect?connectionId=$CONNECTION_ID&tkProspecto=string&tkRazonPerdida=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "tkProspecto": "string",
  "tkRazonPerdida": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/upnify/latest/actions/delete-prospect?${params}`, {
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
| `tkProspecto` | string | yes | El código token que identifica a un prospecto de manera única dentro del CRM, el cual requerimos descartar. ¿Dónde obtengo el token? |
| `tkRazonPerdida` | string | yes | Código token que corresponde a una razón de descartado. ¿Dónde obtengo el token? |

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

Through the native Upnify API, this operation is `DELETE v4/prospectos/:tkProspecto` (base URL `https://api.upnify.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-prospect.md) for the provider-specific parameters and requirements.

