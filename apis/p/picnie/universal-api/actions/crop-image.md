# Picnie: Crop Image

Creates a cropped image in Picnie.

```
POST https://connect.mindcloud.co/v1/universal/picnie/latest/actions/crop-image
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Picnie `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/picnie/latest/actions/crop-image" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "imageUrl": "https://example.com",
  "height": "720",
  "width": "1080",
  "projectId": 1,
  "verticalCropFrom": "center",
  "horizontalCropFrom": "center"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/picnie/latest/actions/crop-image', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "imageUrl": "https://example.com",
    "height": "720",
    "width": "1080",
    "projectId": 1,
    "verticalCropFrom": "center",
    "horizontalCropFrom": "center"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `imageUrl` | string | yes | Image URL to crop. |
| `height` | number | yes | Target crop height. Example: `720`. |
| `width` | number | yes | Target crop width. Example: `1080`. |
| `projectId` | number | yes | Project ID that will own the cropped image. |
| `verticalCropFrom` | string | yes | Vertical crop anchor: top, bottom, or center. Default: `center`. |
| `horizontalCropFrom` | string | yes | Horizontal crop anchor: left, right, or center. Default: `center`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "error": true,
      "message": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `error` | boolean |  |
| `message` | string |  |
| `url` | string |  |

## Native endpoint

Through the native Picnie API, this operation is `POST /crop-image` (base URL `https://picnie.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/crop-image.md) for the provider-specific parameters and requirements.

