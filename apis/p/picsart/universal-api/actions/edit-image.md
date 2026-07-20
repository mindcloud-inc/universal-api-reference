# Picsart: Edit Image

Creates an edited image in Picsart.

```
POST https://connect.mindcloud.co/v1/universal/picsart/latest/actions/edit-image
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Picsart `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/picsart/latest/actions/edit-image" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "imageUrl": "https://pastatic.picsart.com/31399405932227146498.png"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/picsart/latest/actions/edit-image', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "imageUrl": "https://pastatic.picsart.com/31399405932227146498.png"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `imageUrl` | string | yes | Source image URL. Example: `https://pastatic.picsart.com/31399405932227146498.png`. |
| `mode` | string | no | Choose crop or resize mode when applying dimensions. Example: `resize`. |
| `width` | number | no | Output width in pixels. Example: `1200`. |
| `height` | number | no | Output height in pixels. Example: `1200`. |
| `rotate` | number | no | Rotate the image between -180 and 180 degrees. Example: `15`. |
| `format` | string | no | Optional output image format. Example: `PNG`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `flip` | string | no | Flip the image horizontally or vertically. Example: `horizontal`. |

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

Through the native Picsart API, this operation is `POST /tools/1.0/edit` (base URL `https://api.picsart.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/edit-image.md) for the provider-specific parameters and requirements.

