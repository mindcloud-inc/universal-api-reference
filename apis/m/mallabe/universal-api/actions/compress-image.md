# Mallabe: Compress Image

Creates a compressed image in Mallabe.

```
POST https://connect.mindcloud.co/v1/universal/mallabe/latest/actions/compress-image
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mallabe `connectionId` ([setup](../authentication.md)).

## Example request

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

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `url` | string | no | Publicly accessible image URL. |
| `base64Image` | string | no | Base64-encoded image data. |
| `quality` | number | yes | Compression quality for the output image. |
| `fileName` | string | no | Output file name without extension. |
| `fileExtension` | string | no | Output image file extension. |

## Response

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

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `url` | string |  |

## Native endpoint

Through the native Mallabe API, this operation is `POST /images/compress` (base URL `https://mallabe.p.rapidapi.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/compress-image.md) for the provider-specific parameters and requirements.

