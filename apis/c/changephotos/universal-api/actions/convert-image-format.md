# change.photos: Convert Image Format

Creates an image in a new format in change.photos.

```
POST https://connect.mindcloud.co/v1/universal/changephotos/latest/actions/convert-image-format
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a change.photos `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/changephotos/latest/actions/convert-image-format" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "url": "https://example.com/photo.jpg",
  "format": "webp"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/changephotos/latest/actions/convert-image-format', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "url": "https://example.com/photo.jpg",
    "format": "webp"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `url` | string | yes | URL of the image to convert. Example: `https://example.com/photo.jpg`. |
| `format` | list<string> | yes | Output image format. One of: `jpeg`, `png`, `webp`. Example: `webp`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "compression": {},
      "format": "string",
      "height": 1,
      "original": {},
      "processed": {},
      "transformations": {},
      "url": "https://example.com",
      "width": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `compression` | object |  |
| `format` | string | Output image format. |
| `height` | number |  |
| `original` | object |  |
| `processed` | object |  |
| `transformations` | object |  |
| `url` | string | URL to the transformed image. |
| `width` | number |  |

## Native endpoint

Through the native change.photos API, this operation is `POST /api/change` (base URL `https://www.change.photos`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/convert-image-format.md) for the provider-specific parameters and requirements.

