# Mallabe: Resize Image

Creates a resized image in Mallabe.

```
POST https://connect.mindcloud.co/v1/universal/mallabe/latest/actions/resize-image
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mallabe `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/mallabe/latest/actions/resize-image" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "strategy": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mallabe/latest/actions/resize-image', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "strategy": 1
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
| `strategy` | number | yes | Resize strategy code from the Mallabe docs. |
| `width` | number | no | Target width or scale width value. |
| `height` | number | no | Target height or scale height value. |
| `removeExif` | boolean | no | Remove EXIF metadata from the output image. |
| `webhookUrl` | string | no | Webhook URL for asynchronous callbacks. |
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

Through the native Mallabe API, this operation is `POST /images/resize` (base URL `https://mallabe.p.rapidapi.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/resize-image.md) for the provider-specific parameters and requirements.

