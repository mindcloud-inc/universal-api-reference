# change.photos: Transform Image

Creates a transformed image in change.photos.

```
POST https://connect.mindcloud.co/v1/universal/changephotos/latest/actions/transform-image
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a change.photos `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/changephotos/latest/actions/transform-image" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "url": "https://example.com/photo.jpg"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/changephotos/latest/actions/transform-image', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "url": "https://example.com/photo.jpg"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `url` | string | yes | URL of the image to transform. Example: `https://example.com/photo.jpg`. |
| `width` | number | no | Desired width of the output image. Example: `800`. |
| `height` | number | no | Desired height of the output image. Example: `600`. |
| `format` | list<string> | no | Output image format. One of: `jpeg`, `png`, `webp`. Example: `webp`. |
| `quality` | number | no | Output image quality from 1 to 100. Example: `80`. |
| `fit` | list<string> | no | How the image should fit within the dimensions. One of: `contain`, `cover`, `fill`, `inside`, `outside`. Example: `inside`. |
| `flip` | boolean | no | Flip the image vertically. |
| `flop` | boolean | no | Flip the image horizontally. |
| `rotate` | number | no | Rotation angle in degrees from -360 to 360. Example: `45`. |
| `grayscale` | boolean | no | Convert image to grayscale. |
| `blur` | number | no | Gaussian blur sigma value from 0.3 to 1000. Example: `10`. |
| `sharpen` | boolean | no | Apply sharpening effect. |
| `compress` | boolean | no | Apply additional compression. |
| `tint.r` | number | no | Red component of the RGB tint, from 0 to 255. Example: `255`. |
| `tint.g` | number | no | Green component of the RGB tint, from 0 to 255. Example: `200`. |
| `tint.b` | number | no | Blue component of the RGB tint, from 0 to 255. Example: `150`. |

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

Through the native change.photos API, this operation is `POST /api/change` (base URL `https://www.change.photos`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/transform-image.md) for the provider-specific parameters and requirements.

