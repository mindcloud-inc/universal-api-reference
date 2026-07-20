# BBC Sport - Cricket Universal API Examples

These examples use the MindCloud API key and BBC Sport - Cricket connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Cricket Headlines

Retrieves latest BBC Sport cricket headlines.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bBCSportCricket/latest/actions/list-cricket-headlines?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bBCSportCricket/latest/actions/list-cricket-headlines?${params}`, {
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
      "description": "string",
      "id": "string",
      "publishedAt": "2026-05-07T12:00:00.000Z",
      "title": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

See the full [List Cricket Headlines action reference](actions/list-cricket-headlines.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/bBCSportCricket/latest/actions/list-cricket-headlines).
