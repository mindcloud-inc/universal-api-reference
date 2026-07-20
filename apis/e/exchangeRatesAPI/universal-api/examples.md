# Exchange Rates API Universal API Examples

These examples use the MindCloud API key and Exchange Rates API connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Latest Rates

Retrieves latest exchange rates from Exchange Rates API.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/exchangeRatesAPI/latest/actions/get-latest-rates?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/exchangeRatesAPI/latest/actions/get-latest-rates?${params}`, {
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
      "base": "string",
      "date": "2026-05-07T12:00:00.000Z",
      "rates": {},
      "success": true,
      "timestamp": 1
    }
  ],
  "meta": {}
}
```

See the full [Get Latest Rates action reference](actions/get-latest-rates.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/exchangeRatesAPI/latest/actions/get-latest-rates).
