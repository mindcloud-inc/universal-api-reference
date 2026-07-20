# fal.ai Universal API Examples

These examples use the MindCloud API key and fal.ai connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Platform Metadata

Retrieves fal.ai platform metadata and webhook IP ranges.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/falai/latest/actions/get-platform-metadata?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/falai/latest/actions/get-platform-metadata?${params}`, {
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
      "webhook_ip_ranges": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

See the full [Get Platform Metadata action reference](actions/get-platform-metadata.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/falai/latest/actions/get-platform-metadata).

## Create API Key

Creates an API key in fal.ai.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/falai/latest/actions/create-api-key" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "alias": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/falai/latest/actions/create-api-key', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "alias": "string"
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
      "key": "string",
      "key_id": "string",
      "key_secret": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create API Key action reference](actions/create-api-key.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/falai/latest/actions/create-api-key).
