# Golemio API Universal API Examples

These examples use the MindCloud API key and Golemio API connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Parking Sources

Finds parking sources in the Golemio API.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/golemioAPI/latest/actions/list-parking-sources?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/golemioAPI/latest/actions/list-parking-sources?${params}`, {
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
      "contact": {
        "email": "ava@example.com",
        "phone": "string",
        "termOfUseUrl": "https://example.com",
        "webUrl": "https://example.com"
      },
      "name": "Ava Chen",
      "source": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Parking Sources action reference](actions/list-parking-sources.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/golemioAPI/latest/actions/list-parking-sources).
