# Picnie: Add Image Watermark

Creates a watermarked image in Picnie using an image.

```
POST https://connect.mindcloud.co/v1/universal/picnie/latest/actions/add-image-watermark
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Picnie `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/picnie/latest/actions/add-image-watermark" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "projectId": 1,
  "backgroundImageUrl": "https://example.com",
  "frontImageUrl": "https://example.com",
  "position": "br",
  "imageMaxWidth": "800",
  "imageMaxHeight": "800"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/picnie/latest/actions/add-image-watermark', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "projectId": 1,
    "backgroundImageUrl": "https://example.com",
    "frontImageUrl": "https://example.com",
    "position": "br",
    "imageMaxWidth": "800",
    "imageMaxHeight": "800"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `projectId` | number | yes | Project ID that will own the watermarked image. |
| `backgroundImageUrl` | string | yes | Background image URL. |
| `frontImageUrl` | string | yes | Watermark image URL. |
| `position` | string | yes | Watermark position: tl, tc, tr, ml, mc, mr, bl, bc, or br. Default: `br`. |
| `imageMaxWidth` | number | yes | Maximum width of the watermark image. Example: `800`. |
| `imageMaxHeight` | number | yes | Maximum height of the watermark image. Example: `800`. |

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

Through the native Picnie API, this operation is `POST /add-watermark-image` (base URL `https://picnie.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-image-watermark.md) for the provider-specific parameters and requirements.

