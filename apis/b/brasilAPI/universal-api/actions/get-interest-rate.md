# Brasil API: Get Interest Rate

Retrieves an interest rate from Brasil API by symbol.

```
GET https://connect.mindcloud.co/v1/universal/brasilAPI/latest/actions/get-interest-rate
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Brasil API `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/brasilAPI/latest/actions/get-interest-rate?connectionId=$CONNECTION_ID&sigla=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "sigla": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/brasilAPI/latest/actions/get-interest-rate?${params}`, {
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
| `sigla` | string | yes | The interest rate symbol to look up. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "nome": "string",
      "valor": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `nome` | string |  |
| `valor` | number |  |

## Native endpoint

Through the native Brasil API API, this operation is `GET /taxas/v1/{sigla}` (base URL `https://brasilapi.com.br/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-interest-rate.md) for the provider-specific parameters and requirements.

