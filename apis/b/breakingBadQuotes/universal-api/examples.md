# Breaking Bad Quotes Universal API Examples

These examples use the MindCloud API key and Breaking Bad Quotes connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Random Quote



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/breakingBadQuotes/latest/actions/get-random-quote?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/breakingBadQuotes/latest/actions/get-random-quote?${params}`, {
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
      "author": "string",
      "quote": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Random Quote action reference](actions/get-random-quote.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/breakingBadQuotes/latest/actions/get-random-quote).
