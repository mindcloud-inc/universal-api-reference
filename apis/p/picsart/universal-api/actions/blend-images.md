# Picsart: Blend Images

Creates a blended image in Picsart.

```
POST https://connect.mindcloud.co/v1/universal/picsart/latest/actions/blend-images
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Picsart `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/picsart/latest/actions/blend-images" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "imageUrl": "https://pastatic.picsart.com/31399405932227146498.png",
  "overlayImageUrl": "https://cdn.picsart.io/8dee3d34-e90a-4787-a1b4-ed73c4741ee7.jpg"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/picsart/latest/actions/blend-images', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "imageUrl": "https://pastatic.picsart.com/31399405932227146498.png",
    "overlayImageUrl": "https://cdn.picsart.io/8dee3d34-e90a-4787-a1b4-ed73c4741ee7.jpg"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `imageUrl` | string | yes | Base image URL. Example: `https://pastatic.picsart.com/31399405932227146498.png`. |
| `overlayImageUrl` | string | yes | Overlay image URL. Example: `https://cdn.picsart.io/8dee3d34-e90a-4787-a1b4-ed73c4741ee7.jpg`. |
| `opacity` | number | no | Overlay opacity from 0 to 100. Example: `60`. |
| `blendMode` | string | no | Choose how the overlay blends with the base image. Example: `overlay`. |
| `format` | string | no | Optional output image format. Example: `PNG`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "id": "string",
        "url": "https://example.com"
      },
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data.id` | string |  |
| `data.url` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Picsart API, this operation is `POST /tools/1.0/blend` (base URL `https://api.picsart.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/blend-images.md) for the provider-specific parameters and requirements.

