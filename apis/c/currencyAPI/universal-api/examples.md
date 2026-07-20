# CurrencyAPI Universal API Examples

These examples use the MindCloud API key and CurrencyAPI connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get API Status

Retrieves current API quota status from CurrencyAPI.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/currencyAPI/latest/actions/get-api-status?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/currencyAPI/latest/actions/get-api-status?${params}`, {
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
      "accountId": 1,
      "quotas": {}
    }
  ],
  "meta": {}
}
```

See the full [Get API Status action reference](actions/get-api-status.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/currencyAPI/latest/actions/get-api-status).
