# The Odds Universal API Examples

These examples use the MindCloud API key and The Odds connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Sports

Retrieves supported sports from The Odds API.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/theOddsAPI/latest/actions/list-sports?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/theOddsAPI/latest/actions/list-sports?${params}`, {
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
      "active": true,
      "description": "string",
      "group": "string",
      "has_outrights": true,
      "key": "string",
      "title": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Sports action reference](actions/list-sports.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/theOddsAPI/latest/actions/list-sports).
