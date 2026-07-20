# Picnie: Add Text Watermark

Creates a watermarked image in Picnie using text.

```
POST https://connect.mindcloud.co/v1/universal/picnie/latest/actions/add-text-watermark
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Picnie `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/picnie/latest/actions/add-text-watermark" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "imageUrl": "https://example.com",
  "projectId": 1,
  "watermarkText": "© 2026 MindCloud",
  "position": "bottom-right",
  "fontSize": "32",
  "fontPath": "Anton-Regular.ttf",
  "fontColor": "#FF0000",
  "opacity": "0.8",
  "rotation": "45",
  "padding": "20",
  "backgroundColor": "#000000",
  "backgroundOpacity": "0.5"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/picnie/latest/actions/add-text-watermark', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "imageUrl": "https://example.com",
    "projectId": 1,
    "watermarkText": "© 2026 MindCloud",
    "position": "bottom-right",
    "fontSize": "32",
    "fontPath": "Anton-Regular.ttf",
    "fontColor": "#FF0000",
    "opacity": "0.8",
    "rotation": "45",
    "padding": "20",
    "backgroundColor": "#000000",
    "backgroundOpacity": "0.5"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `imageUrl` | string | yes | Image URL to watermark with text. |
| `projectId` | number | yes | Project ID that will own the watermarked image. |
| `watermarkText` | string | yes | Text to render as the watermark. Example: `© 2026 MindCloud`. |
| `position` | string | yes | Watermark position such as bottom-right. Default: `bottom-right`. |
| `fontSize` | number | yes | Font size in pixels. Example: `32`. |
| `fontPath` | string | yes | Font path or font filename. Default: `Anton-Regular.ttf`. |
| `fontColor` | string | yes | Text color in hex. Default: `#FF0000`. |
| `opacity` | number | yes | Text opacity between 0.0 and 1.0. Default: `0.8`. |
| `rotation` | number | yes | Rotation angle in degrees. Default: `45`. |
| `padding` | number | yes | Padding around the watermark in pixels. Default: `20`. |
| `backgroundColor` | string | yes | Background color in hex. Default: `#000000`. |
| `backgroundOpacity` | number | yes | Background opacity between 0.0 and 1.0. Default: `0.5`. |

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

Through the native Picnie API, this operation is `POST /add-watermark-text-on-image` (base URL `https://picnie.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-text-watermark.md) for the provider-specific parameters and requirements.

