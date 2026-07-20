# TinyPNG Universal API Examples

These examples use the MindCloud API key and TinyPNG connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Download Optimized Image

Downloads an optimized image from TinyPNG.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tinyPNG/latest/actions/download-optimized-image?connectionId=$CONNECTION_ID&outputPath=%2Foutput%2Fabc123" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "outputPath": "/output/abc123"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tinyPNG/latest/actions/download-optimized-image?${params}`, {
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
      "compressionCount": 1,
      "contentLength": 1,
      "contentType": "string",
      "imageHeight": 1,
      "imageWidth": 1
    }
  ],
  "meta": {}
}
```

See the full [Download Optimized Image action reference](actions/download-optimized-image.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/tinyPNG/latest/actions/download-optimized-image).

## Compress Image From URL

Compresses an image from a URL with TinyPNG.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/tinyPNG/latest/actions/compress-image-from-url" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "imageUrl": "https://tinypng.com/images/panda-happy.png"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/tinyPNG/latest/actions/compress-image-from-url', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "imageUrl": "https://tinypng.com/images/panda-happy.png"
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

See the full [Compress Image From URL action reference](actions/compress-image-from-url.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/tinyPNG/latest/actions/compress-image-from-url).
