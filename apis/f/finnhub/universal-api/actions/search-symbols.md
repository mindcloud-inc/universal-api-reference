# Finnhub: Search Symbols

Finds symbols in Finnhub by search text.

```
GET https://connect.mindcloud.co/v1/universal/finnhub/latest/actions/search-symbols
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Finnhub `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/finnhub/latest/actions/search-symbols?connectionId=$CONNECTION_ID&q=e.g.%20Apple" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "q": "e.g. Apple"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/finnhub/latest/actions/search-symbols?${params}`, {
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
| `q` | string | yes | Search text. Finnhub accepts a symbol, security name, ISIN, or CUSIP. Example: `e.g. Apple`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `exchange` | string | no | Optional exchange limit for symbol search. Example: `e.g. US`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "count": 1,
      "result": {
        "description": "string",
        "displaySymbol": "string",
        "symbol": "string",
        "type": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `count` | number |  |
| `result` | array<object> |  |
| `result.description` | string |  |
| `result.displaySymbol` | string |  |
| `result.symbol` | string |  |
| `result.type` | string |  |

## Native endpoint

Through the native Finnhub API, this operation is `GET /search` (base URL `https://finnhub.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-symbols.md) for the provider-specific parameters and requirements.

