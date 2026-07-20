# Ron Swanson Quotes Universal API Examples

These examples use the MindCloud API key and Ron Swanson Quotes connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Quotes

Retrieves multiple Ron Swanson quotes.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ronSwansonQuotes/latest/actions/get-quotes?connectionId=$CONNECTION_ID&count=2" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "count": "2"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ronSwansonQuotes/latest/actions/get-quotes?${params}`, {
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
      "quote": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Quotes action reference](actions/get-quotes.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/ronSwansonQuotes/latest/actions/get-quotes).
