# change.photos: Blur Image

Creates a blurred image in change.photos.

```
POST https://connect.mindcloud.co/v1/universal/changephotos/latest/actions/blur-image
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a change.photos `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/changephotos/latest/actions/blur-image" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "url": "https://example.com/photo.jpg",
  "blur": "10"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/changephotos/latest/actions/blur-image', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "url": "https://example.com/photo.jpg",
    "blur": "10"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `url` | string | yes | URL of the image to blur. Example: `https://example.com/photo.jpg`. |
| `blur` | number | yes | Gaussian blur sigma value from 0.3 to 1000. Example: `10`. |

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

Through the native change.photos API, this operation is `POST /api/change` (base URL `https://www.change.photos`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/blur-image.md) for the provider-specific parameters and requirements.

