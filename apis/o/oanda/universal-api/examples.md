# Oanda Universal API Examples

These examples use the MindCloud API key and Oanda connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Remaining Quotes

Retrieves remaining quote usage from Oanda.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/oanda/latest/actions/get-remaining-quotes?connectionId=$CONNECTION_ID&ext=json" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "ext": "json"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/oanda/latest/actions/get-remaining-quotes?${params}`, {
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
      "remaining_quotes": "string",
      "used_quotes": 1
    }
  ],
  "meta": {}
}
```

See the full [Get Remaining Quotes action reference](actions/get-remaining-quotes.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/oanda/latest/actions/get-remaining-quotes).
