# Financial Modeling Prep: Search Stock Symbols

Finds stock symbols in Financial Modeling Prep by search query.

```
GET https://connect.mindcloud.co/v1/universal/financialModelingPrep/latest/actions/search-stock-symbols
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Financial Modeling Prep `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/financialModelingPrep/latest/actions/search-stock-symbols?connectionId=$CONNECTION_ID&query=AAPL" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "query": "AAPL"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/financialModelingPrep/latest/actions/search-stock-symbols?${params}`, {
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
| `query` | string | yes | Ticker symbol or company name to search for, such as AAPL. Example: `AAPL`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "currency": "string",
      "exchange": "string",
      "exchangeFullName": "Ava Chen",
      "name": "Ava Chen",
      "symbol": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `currency` | string | Trading currency. |
| `exchange` | string | Exchange code. |
| `exchangeFullName` | string | Full exchange name. |
| `name` | string | Company or instrument name. |
| `symbol` | string | Ticker symbol. |

## Native endpoint

Through the native Financial Modeling Prep API, this operation is `GET /search-symbol` (base URL `https://financialmodelingprep.com/stable`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-stock-symbols.md) for the provider-specific parameters and requirements.

