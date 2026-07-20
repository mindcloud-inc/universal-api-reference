# Brasil API: Get IBGE State

Retrieves an IBGE state from Brasil API by code.

```
GET https://connect.mindcloud.co/v1/universal/brasilAPI/latest/actions/get-ibge-state
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Brasil API `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/brasilAPI/latest/actions/get-ibge-state?connectionId=$CONNECTION_ID&code=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "code": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/brasilAPI/latest/actions/get-ibge-state?${params}`, {
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
| `code` | string | yes | The IBGE state code or abbreviation. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": 1,
      "nome": "string",
      "regiao": {},
      "sigla": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number |  |
| `nome` | string |  |
| `regiao` | object |  |
| `sigla` | string |  |

## Native endpoint

Through the native Brasil API API, this operation is `GET /ibge/uf/v1/{code}` (base URL `https://brasilapi.com.br/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-ibge-state.md) for the provider-specific parameters and requirements.

