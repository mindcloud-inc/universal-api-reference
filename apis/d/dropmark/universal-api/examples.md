# Dropmark Universal API Examples

These examples use the MindCloud API key and Dropmark connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Activity



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dropmark/latest/actions/get-activity?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dropmark/latest/actions/get-activity?${params}`, {
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
      "id": 1,
      "name": "Ava Chen",
      "type": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

See the full [Get Activity action reference](actions/get-activity.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/dropmark/latest/actions/get-activity).
