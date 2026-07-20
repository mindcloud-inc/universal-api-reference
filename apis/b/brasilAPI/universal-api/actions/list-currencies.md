# Brasil API: List Currencies

Retrieves available currencies from Brasil API.

```
GET https://connect.mindcloud.co/v1/universal/brasilAPI/latest/actions/list-currencies
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Brasil API `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/brasilAPI/latest/actions/list-currencies?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/brasilAPI/latest/actions/list-currencies?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "nome": "string",
      "simbolo": "string",
      "tipo_moeda": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `nome` | string |  |
| `simbolo` | string |  |
| `tipo_moeda` | string |  |

## Native endpoint

Through the native Brasil API API, this operation is `GET /cambio/v1/moedas` (base URL `https://brasilapi.com.br/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-currencies.md) for the provider-specific parameters and requirements.

