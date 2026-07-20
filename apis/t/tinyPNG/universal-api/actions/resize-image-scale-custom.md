# TinyPNG: Resize Image Scale Custom

Creates a TinyPNG image scaled to a custom size.

```
POST https://connect.mindcloud.co/v1/universal/tinyPNG/latest/actions/resize-image-scale-custom
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TinyPNG `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/tinyPNG/latest/actions/resize-image-scale-custom" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "outputPath": "/output/abc123"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/tinyPNG/latest/actions/resize-image-scale-custom', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "outputPath": "/output/abc123"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `outputPath` | string | yes | TinyPNG output path returned by a previous action, for example `/output/abc123`. Example: `/output/abc123`. |
| `width` | number | no | Target width in pixels. Use either width or height, but not both. |
| `height` | number | no | Target height in pixels. Use either width or height, but not both. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "compressionCount": 1,
      "contentLength": 1,
      "contentType": "string",
      "imageHeight": 1,
      "imageWidth": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `compressionCount` | number |  |
| `contentLength` | number |  |
| `contentType` | string |  |
| `imageHeight` | number |  |
| `imageWidth` | number |  |

## Native endpoint

Through the native TinyPNG API, this operation is `POST {{outputPath}}` (base URL `https://api.tinify.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/resize-image-scale-custom.md) for the provider-specific parameters and requirements.

