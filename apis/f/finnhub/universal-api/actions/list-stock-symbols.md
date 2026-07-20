# Finnhub: List Stock Symbols

Retrieves stock symbols from Finnhub.

```
GET https://connect.mindcloud.co/v1/universal/finnhub/latest/actions/list-stock-symbols
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Finnhub `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/finnhub/latest/actions/list-stock-symbols?connectionId=$CONNECTION_ID&exchange=e.g.%20US" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "exchange": "e.g. US"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/finnhub/latest/actions/list-stock-symbols?${params}`, {
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
| `exchange` | string | yes | Exchange code for supported stock symbols, such as US. Example: `e.g. US`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `mic` | string | no | Optional MIC code filter. Example: `e.g. XNAS`. |
| `securityType` | string | no | Optional security type filter using OpenFIGI security type values. Example: `e.g. Common Stock`. |
| `currency` | string | no | Optional currency filter. Example: `e.g. USD`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "currency": "string",
      "description": "string",
      "displaySymbol": "string",
      "figi": "string",
      "figiComposite": "string",
      "isin": "string",
      "mic": "string",
      "shareClassFIGI": "string",
      "symbol": "string",
      "symbol2": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `currency` | string |  |
| `description` | string |  |
| `displaySymbol` | string |  |
| `figi` | string |  |
| `figiComposite` | string |  |
| `isin` | string |  |
| `mic` | string |  |
| `shareClassFIGI` | string |  |
| `symbol` | string |  |
| `symbol2` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Finnhub API, this operation is `GET /stock/symbol` (base URL `https://finnhub.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-stock-symbols.md) for the provider-specific parameters and requirements.

