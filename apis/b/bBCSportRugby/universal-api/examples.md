# BBC Sport - Rugby Universal API Examples

These examples use the MindCloud API key and BBC Sport - Rugby connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Bath Rugby Headlines

Retrieves Bath rugby headlines from BBC Sport - Rugby.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bBCSportRugby/latest/actions/list-bath-rugby-headlines?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bBCSportRugby/latest/actions/list-bath-rugby-headlines?${params}`, {
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
      "description": {},
      "guid": "string",
      "link": "https://example.com",
      "pubDate": "2026-05-07T12:00:00.000Z",
      "title": {}
    }
  ],
  "meta": {}
}
```

See the full [List Bath Rugby Headlines action reference](actions/list-bath-rugby-headlines.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/bBCSportRugby/latest/actions/list-bath-rugby-headlines).
