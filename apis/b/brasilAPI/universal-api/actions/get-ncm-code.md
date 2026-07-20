# Brasil API: Get NCM Code

Retrieves an NCM code from Brasil API by code.

```
GET https://connect.mindcloud.co/v1/universal/brasilAPI/latest/actions/get-ncm-code
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Brasil API `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/brasilAPI/latest/actions/get-ncm-code?connectionId=$CONNECTION_ID&code=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "code": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/brasilAPI/latest/actions/get-ncm-code?${params}`, {
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
| `code` | string | yes | The NCM code to look up. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "ano_ato": "string",
      "codigo": "string",
      "data_fim": "string",
      "data_inicio": "string",
      "descricao": "string",
      "numero_ato": "string",
      "tipo_ato": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `ano_ato` | string |  |
| `codigo` | string |  |
| `data_fim` | string |  |
| `data_inicio` | string |  |
| `descricao` | string |  |
| `numero_ato` | string |  |
| `tipo_ato` | string |  |

## Native endpoint

Through the native Brasil API API, this operation is `GET /ncm/v1/{code}` (base URL `https://brasilapi.com.br/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-ncm-code.md) for the provider-specific parameters and requirements.

