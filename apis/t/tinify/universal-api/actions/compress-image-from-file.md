# Tinify: Compress Image From File

Compresses an uploaded image file in Tinify.

```
POST https://connect.mindcloud.co/v1/universal/tinify/latest/actions/compress-image-from-file
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tinify `connectionId` ([setup](../authentication.md)).

## Example request

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

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `file` | file | yes | AVIF, WebP, JPEG, or PNG image file to optimize. Example: `Upload a PNG, JPEG, WebP, or AVIF image file`. |

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
| `output.height` | number | Optimized image height in pixels when returned by Tinify. |
| `output.ratio` | number | Compression ratio when returned by Tinify. |
| `output.size` | number | Optimized image size in bytes when returned by Tinify. |
| `output.type` | string | Optimized image MIME type when returned by Tinify. |
| `output.url` | string | Tinify output URL for the optimized image when returned by Tinify. |
| `output.width` | number | Optimized image width in pixels when returned by Tinify. |

## Native endpoint

Through the native Tinify API, this operation is `POST /shrink` (base URL `https://api.tinify.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/compress-image-from-file.md) for the provider-specific parameters and requirements.

