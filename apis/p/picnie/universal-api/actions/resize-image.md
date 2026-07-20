# Picnie: Resize Image

Creates a resized image in Picnie.

```
POST https://connect.mindcloud.co/v1/universal/picnie/latest/actions/resize-image
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Picnie `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/picnie/latest/actions/resize-image" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "projectId": 1,
  "imageUrl": "https://example.com",
  "resizeType": "1",
  "height": "500",
  "width": "800"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/picnie/latest/actions/resize-image', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "projectId": 1,
    "imageUrl": "https://example.com",
    "resizeType": "1",
    "height": "500",
    "width": "800"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `projectId` | number | yes | Project ID that will own the resized image. |
| `imageUrl` | string | yes | Image URL to resize. |
| `resizeType` | string | yes | 1 for height and width, 2 for percentage resize. Default: `1`. |
| `height` | number | yes | Target height when resize type is 1. Example: `500`. |
| `width` | number | yes | Target width when resize type is 1. Example: `800`. |
| `resizePercentage` | number | no | Resize percentage when resize type is 2. Example: `50`. |
| `noEnlargeOnSmaller` | string | no | Set to 1 to avoid enlarging smaller images. Example: `1`. |
| `isMaintainAspectRatio` | string | no | Set to 1 to preserve aspect ratio. Example: `1`. |

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

Through the native Picnie API, this operation is `POST /resize-image` (base URL `https://picnie.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/resize-image.md) for the provider-specific parameters and requirements.

