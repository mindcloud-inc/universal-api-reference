# Slashdot Universal API Examples

These examples use the MindCloud API key and Slashdot connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Main Feed

Retrieves the main feed from Slashdot.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/slashdot/latest/actions/get-main-feed?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/slashdot/latest/actions/get-main-feed?${params}`, {
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
      "dc:creator": "string",
      "dc:date": "2026-05-07T12:00:00.000Z",
      "dc:subject": "string",
      "description": "string",
      "link": "https://example.com",
      "slash:comments": "string",
      "slash:department": "string",
      "slash:hit_parade": "string",
      "slash:section": "string",
      "title": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Main Feed action reference](actions/get-main-feed.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/slashdot/latest/actions/get-main-feed).
