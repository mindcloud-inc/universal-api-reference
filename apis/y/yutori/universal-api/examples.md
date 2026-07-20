# Yutori Universal API Examples

These examples use the MindCloud API key and Yutori connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Health

Retrieves the current Yutori API health status.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/yutori/latest/actions/get-health?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/yutori/latest/actions/get-health?${params}`, {
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
      "status": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Health action reference](actions/get-health.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/yutori/latest/actions/get-health).

## Bulk Subscribe to Scout

Creates email subscriptions for a scout in Yutori.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/yutori/latest/actions/bulk-subscribe-to-scout" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "scoutId": "string",
  "emails[]": [
    "ava@example.com"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/yutori/latest/actions/bulk-subscribe-to-scout', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "scoutId": "string",
    "emails[]": ["ava@example.com"]
  })
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [],
  "meta": {}
}
```

See the full [Bulk Subscribe to Scout action reference](actions/bulk-subscribe-to-scout.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/yutori/latest/actions/bulk-subscribe-to-scout).
