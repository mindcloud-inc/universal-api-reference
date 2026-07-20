# Mallabe Universal API Examples

These examples use the MindCloud API key and Mallabe connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Image Metadata

Retrieves metadata for an image from Mallabe.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mallabe/latest/actions/get-image-metadata?connectionId=$CONNECTION_ID&url=https%3A%2F%2Fexample.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "url": "https://example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mallabe/latest/actions/get-image-metadata?${params}`, {
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
      "channels": 1,
      "density": 1,
      "depth": "string",
      "format": "string",
      "hasAlpha": true,
      "hasProfile": true,
      "height": 1,
      "isProgressive": true,
      "width": 1
    }
  ],
  "meta": {}
}
```

See the full [Get Image Metadata action reference](actions/get-image-metadata.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/mallabe/latest/actions/get-image-metadata).

## Compress Image

Creates a compressed image in Mallabe.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/mallabe/latest/actions/compress-image" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "quality": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mallabe/latest/actions/compress-image', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "quality": 1
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
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

See the full [Compress Image action reference](actions/compress-image.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/mallabe/latest/actions/compress-image).
