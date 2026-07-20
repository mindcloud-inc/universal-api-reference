# Brasil API: Get Exchange Rate

Retrieves a BRL exchange rate from Brasil API by currency and date.

```
GET https://connect.mindcloud.co/v1/universal/brasilAPI/latest/actions/get-exchange-rate
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Brasil API `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/brasilAPI/latest/actions/get-exchange-rate?connectionId=$CONNECTION_ID&moeda=string&data=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "moeda": "string",
  "data": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/brasilAPI/latest/actions/get-exchange-rate?${params}`, {
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
| `moeda` | string | yes | The target currency code to quote against BRL. |
| `data` | string | yes | The quote date in YYYY-MM-DD format. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "cotacoes": [
        {}
      ],
      "data": "string",
      "moeda": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `cotacoes` | array<object> |  |
| `data` | string |  |
| `moeda` | string |  |

## Native endpoint

Through the native Brasil API API, this operation is `GET /cambio/v1/cotacao/{moeda}/{data}` (base URL `https://brasilapi.com.br/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-exchange-rate.md) for the provider-specific parameters and requirements.

