# Launch Library 2 Universal API Examples

These examples use the MindCloud API key and Launch Library 2 connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Agency



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/launchLibrary2/latest/actions/get-agency?connectionId=$CONNECTION_ID&id=121" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "121"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/launchLibrary2/latest/actions/get-agency?${params}`, {
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
      "abbrev": "string",
      "country": [
        {}
      ],
      "description": "string",
      "featured": true,
      "founding_year": 1,
      "id": 1,
      "name": "Ava Chen",
      "type": {
        "name": "Ava Chen"
      },
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

See the full [Get Agency action reference](actions/get-agency.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/launchLibrary2/latest/actions/get-agency).
