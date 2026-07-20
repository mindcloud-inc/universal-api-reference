# Finnhub Universal API Examples

These examples use the MindCloud API key and Finnhub connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Stock Quote

Retrieves a stock quote from Finnhub.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/finnhub/latest/actions/get-stock-quote?connectionId=$CONNECTION_ID&symbol=e.g.%20AAPL" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "symbol": "e.g. AAPL"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/finnhub/latest/actions/get-stock-quote?${params}`, {
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
      "c": 1,
      "d": 1,
      "dp": 1,
      "h": 1,
      "l": 1,
      "o": 1,
      "pc": 1,
      "t": 1
    }
  ],
  "meta": {}
}
```

See the full [Get Stock Quote action reference](actions/get-stock-quote.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/finnhub/latest/actions/get-stock-quote).
