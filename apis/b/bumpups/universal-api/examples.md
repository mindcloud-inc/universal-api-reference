# Bumpups Universal API Examples

These examples use the MindCloud API key and Bumpups connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Condition Assessment

Creates a condition assessment from a video in Bumpups.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/bumpups/latest/actions/condition-assessment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "url": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/bumpups/latest/actions/condition-assessment', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "url": "https://example.com"
  })
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [
    {
      "language": "string",
      "model": "string",
      "output": "string",
      "outputFormat": "string",
      "prompt": "string",
      "url": "https://example.com",
      "videoDuration": 1
    }
  ],
  "meta": {}
}
```

See the full [Condition Assessment action reference](actions/condition-assessment.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/bumpups/latest/actions/condition-assessment).
