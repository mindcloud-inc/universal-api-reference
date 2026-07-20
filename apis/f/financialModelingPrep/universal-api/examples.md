# Financial Modeling Prep Universal API Examples

These examples use the MindCloud API key and Financial Modeling Prep connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Search Stock Symbols

Finds stock symbols in Financial Modeling Prep by search query.

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

Example response:

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

See the full [Search Stock Symbols action reference](actions/search-stock-symbols.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/financialModelingPrep/latest/actions/search-stock-symbols).
