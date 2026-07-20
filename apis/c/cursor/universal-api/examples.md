# Cursor Universal API Examples

These examples use the MindCloud API key and Cursor connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## API Key Info



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cursor/latest/actions/api-key-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cursor/latest/actions/api-key-info?${params}`, {
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
      "apiKeyName": "Ava Chen",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "userEmail": "ava@example.com"
    }
  ],
  "meta": {}
}
```

See the full [API Key Info action reference](actions/api-key-info.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/cursor/latest/actions/api-key-info).

## Add Followup



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/cursor/latest/actions/add-followup" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "bc_abc123",
  "prompt.text": "Also add a section about troubleshooting"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/cursor/latest/actions/add-followup', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "bc_abc123",
    "prompt.text": "Also add a section about troubleshooting"
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
      "id": "string"
    }
  ],
  "meta": {}
}
```

See the full [Add Followup action reference](actions/add-followup.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/cursor/latest/actions/add-followup).
