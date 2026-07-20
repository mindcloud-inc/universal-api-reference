# Tinify: Compress Image From URL

Compresses an image from a URL in Tinify.

```
POST https://connect.mindcloud.co/v1/universal/tinify/latest/actions/compress-image-from-url
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tinify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/tinify/latest/actions/compress-image-from-url" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "source.url": "https://tinypng.com/images/panda-happy.png"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/tinify/latest/actions/compress-image-from-url', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "source.url": "https://tinypng.com/images/panda-happy.png"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `source.url` | string | yes | Publicly reachable AVIF, WebP, JPEG, or PNG image URL to optimize. Default: `https://tinypng.com/images/panda-happy.png`. Example: `https://tinypng.com/images/panda-happy.png`. |

## Response

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

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `input.size` | number | Original image size in bytes. |
| `input.type` | string | Original image MIME type. |
| `output.height` | number | Compressed image height in pixels. |
| `output.ratio` | number | Compression ratio between input and output. |
| `output.size` | number | Compressed image size in bytes. |
| `output.type` | string | Compressed image MIME type. |
| `output.url` | string | Tinify output URL for the compressed image. |
| `output.width` | number | Compressed image width in pixels. |

## Native endpoint

Through the native Tinify API, this operation is `POST /shrink` (base URL `https://api.tinify.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/compress-image-from-url.md) for the provider-specific parameters and requirements.

