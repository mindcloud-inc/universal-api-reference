# eGestor: Delete Service

Deletes an existing service from eGestor.

```
DELETE https://connect.mindcloud.co/v1/universal/eGestor/latest/actions/delete-service
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a eGestor `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/eGestor/latest/actions/delete-service?connectionId=$CONNECTION_ID&codigo=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "codigo": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eGestor/latest/actions/delete-service?${params}`, {
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
| `codigo` | number | yes | Código do serviço. Example: `1`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": "string",
      "fields": "string",
      "msg": "string",
      "obs": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | string |  |
| `fields` | string |  |
| `msg` | string |  |
| `obs` | string |  |

## Native endpoint

Through the native eGestor API, this operation is `DELETE /servicos/:codigo` (base URL `https://api.egestor.com.br/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-service.md) for the provider-specific parameters and requirements.

