# finlight Universal API Examples

These examples use the MindCloud API key and finlight connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Sources

Retrieves supported news sources from finlight.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/finlight/latest/actions/list-sources?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/finlight/latest/actions/list-sources?${params}`, {
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
      "domain": "string",
      "isDefaultSource": true,
      "originCountry": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Sources action reference](actions/list-sources.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/finlight/latest/actions/list-sources).
