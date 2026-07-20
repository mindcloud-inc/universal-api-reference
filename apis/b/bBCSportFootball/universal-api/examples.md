# BBC Sport - Football Universal API Examples

These examples use the MindCloud API key and BBC Sport - Football connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Football Africa Articles



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bBCSportFootball/latest/actions/list-football-africa-articles?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bBCSportFootball/latest/actions/list-football-africa-articles?${params}`, {
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
      "guid": "string",
      "link": "https://example.com",
      "publishedAt": "string",
      "thumbnailUrl": "https://example.com",
      "title": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Football Africa Articles action reference](actions/list-football-africa-articles.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/bBCSportFootball/latest/actions/list-football-africa-articles).
