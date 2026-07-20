# Tinify Universal API Examples

These examples use the MindCloud API key and Tinify connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Download Optimized Image

Downloads an optimized image from Tinify.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tinify/latest/actions/download-optimized-image?connectionId=$CONNECTION_ID&outputId=zr1jp6xybr82ge0s683x67rgwsawjw4z" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "outputId": "zr1jp6xybr82ge0s683x67rgwsawjw4z"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tinify/latest/actions/download-optimized-image?${params}`, {
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
      "data": [
        1
      ],
      "type": "string"
    }
  ],
  "meta": {}
}
```

See the full [Download Optimized Image action reference](actions/download-optimized-image.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/tinify/latest/actions/download-optimized-image).

## Compress Image From File

Compresses an uploaded image file in Tinify.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/tinify/latest/actions/compress-image-from-file" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "file": "Upload a PNG, JPEG, WebP, or AVIF image file"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/tinify/latest/actions/compress-image-from-file', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "file": "Upload a PNG, JPEG, WebP, or AVIF image file"
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
      "input": {
        "size": 1,
        "type": "string"
      },
      "output": {
        "height": 1,
        "ratio": 1,
        "size": 1,
        "type": "string",
        "url": "https://example.com",
        "width": 1
      }
    }
  ],
  "meta": {}
}
```

See the full [Compress Image From File action reference](actions/compress-image-from-file.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/tinify/latest/actions/compress-image-from-file).
