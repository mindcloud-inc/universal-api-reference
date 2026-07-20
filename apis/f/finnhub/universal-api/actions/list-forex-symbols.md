# Finnhub: List Forex Symbols

Retrieves forex symbols from Finnhub.

```
GET https://connect.mindcloud.co/v1/universal/finnhub/latest/actions/list-forex-symbols
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Finnhub `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/finnhub/latest/actions/list-forex-symbols?connectionId=$CONNECTION_ID&exchange=e.g.%20oanda" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "exchange": "e.g. oanda"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/finnhub/latest/actions/list-forex-symbols?${params}`, {
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
| `exchange` | string | yes | Forex exchange code, such as oanda. Example: `e.g. oanda`. |

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

Through the native Finnhub API, this operation is `GET /forex/symbol` (base URL `https://finnhub.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-forex-symbols.md) for the provider-specific parameters and requirements.

