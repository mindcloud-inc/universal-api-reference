# Finnhub: List Crypto Symbols

Retrieves crypto symbols from Finnhub.

```
GET https://connect.mindcloud.co/v1/universal/finnhub/latest/actions/list-crypto-symbols
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Finnhub `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/finnhub/latest/actions/list-crypto-symbols?connectionId=$CONNECTION_ID&exchange=e.g.%20binance" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "exchange": "e.g. binance"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/finnhub/latest/actions/list-crypto-symbols?${params}`, {
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
| `exchange` | string | yes | Crypto exchange code, such as binance. Example: `e.g. binance`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "description": "string",
      "displaySymbol": "string",
      "symbol": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `description` | string |  |
| `displaySymbol` | string |  |
| `symbol` | string |  |

## Native endpoint

Through the native Finnhub API, this operation is `GET /crypto/symbol` (base URL `https://finnhub.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-crypto-symbols.md) for the provider-specific parameters and requirements.

