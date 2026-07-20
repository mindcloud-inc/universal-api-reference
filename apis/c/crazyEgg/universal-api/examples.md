# Crazy Egg Universal API Examples

These examples use the MindCloud API key and Crazy Egg connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Authenticate API Signature



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/crazyEgg/latest/actions/authenticate-api-signature?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/crazyEgg/latest/actions/authenticate-api-signature?${params}`, {
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
      "msg": "string"
    }
  ],
  "meta": {}
}
```

See the full [Authenticate API Signature action reference](actions/authenticate-api-signature.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/crazyEgg/latest/actions/authenticate-api-signature).

## Create Snapshot



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/crazyEgg/latest/actions/create-snapshot" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "snapshot.sourceUrl": "https://example.com",
  "snapshot.name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/crazyEgg/latest/actions/create-snapshot', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "snapshot.sourceUrl": "https://example.com",
    "snapshot.name": "Ava Chen"
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
      "description": "string",
      "device": "string",
      "expires_at": "string",
      "heatmap_generation_status": "string",
      "heatmap_url": "https://example.com",
      "id": "string",
      "max_visits": 1,
      "name": "Ava Chen",
      "processing_status": "string",
      "sampling_ratio": 1,
      "screenshot_url": "https://example.com",
      "source_url": "https://example.com",
      "starts_at": "string",
      "status": "string",
      "thumbnail_url": "https://example.com",
      "url_matching_rules": "https://example.com"
    }
  ],
  "meta": {}
}
```

See the full [Create Snapshot action reference](actions/create-snapshot.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/crazyEgg/latest/actions/create-snapshot).
