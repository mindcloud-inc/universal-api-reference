# Cloudinary Universal API Examples

These examples use the MindCloud API key and Cloudinary connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Ping

Pings the Cloudinary Admin API connection.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cloudinary/latest/actions/ping?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cloudinary/latest/actions/ping?${params}`, {
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

See the full [Ping action reference](actions/ping.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/cloudinary/latest/actions/ping).

## Apply Explicit Asset Actions

Applies explicit asset actions in Cloudinary.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/cloudinary/latest/actions/apply-explicit-asset-actions" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "publicId": "string",
  "resourceType": "string",
  "type": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/cloudinary/latest/actions/apply-explicit-asset-actions', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "publicId": "string",
    "resourceType": "string",
    "type": "string"
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
      "asset_folder": "string",
      "asset_id": "string",
      "bytes": 1,
      "created_at": "string",
      "display_name": "Ava Chen",
      "format": "string",
      "height": 1,
      "placeholder": true,
      "public_id": "string",
      "resource_type": "string",
      "secure_url": "https://example.com",
      "signature": "string",
      "tags": [
        "string"
      ],
      "type": "string",
      "url": "https://example.com",
      "version": 1,
      "version_id": "string",
      "width": 1
    }
  ],
  "meta": {}
}
```

See the full [Apply Explicit Asset Actions action reference](actions/apply-explicit-asset-actions.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/cloudinary/latest/actions/apply-explicit-asset-actions).
