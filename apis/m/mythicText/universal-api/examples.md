# Mythic Text Universal API Examples

These examples use the MindCloud API key and Mythic Text connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Connection Check



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mythicText/latest/actions/connection-check?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mythicText/latest/actions/connection-check?${params}`, {
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
      "html": "string",
      "model": "string",
      "processing_time_ms": 1
    }
  ],
  "meta": {}
}
```

See the full [Connection Check action reference](actions/connection-check.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/mythicText/latest/actions/connection-check).
