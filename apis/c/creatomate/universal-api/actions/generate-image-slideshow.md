# Creatomate: Generate Image Slideshow

Creates an image slideshow render in Creatomate.

```
POST https://connect.mindcloud.co/v1/universal/creatomate/latest/actions/generate-image-slideshow
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Creatomate `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/creatomate/latest/actions/generate-image-slideshow" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "imageUrls[]": [
    "https://example.com"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/creatomate/latest/actions/generate-image-slideshow', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "imageUrls[]": ["https://example.com"]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `imageUrls[]` | array<string> | yes | Ordered list of image URLs to include in the slideshow. |
| `imageDurationSeconds` | number | no | How long each image should stay on screen before the next one. Default: `5`. |
| `includeTransitions` | boolean | no | Whether to add the documented transition animation between images. Default: `true`. |
| `includeZoomOut` | boolean | no | Whether to add the documented zoom-out effect to each image. Default: `false`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `transitionType` | string | no | Creatomate transition type to apply between images. Default: `slide`. |
| `transitionDirection` | string | no | Direction used by the slide transition. Default: `180°`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "outputFormat": "string",
      "status": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string | Creatomate render ID. |
| `outputFormat` | string | Output format requested for the render. |
| `status` | string | Current render status returned by Creatomate. |
| `url` | string | Direct URL for the rendered output file. |

## Native endpoint

Through the native Creatomate API, this operation is `POST /v2/renders` (base URL `https://api.creatomate.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/generate-image-slideshow.md) for the provider-specific parameters and requirements.

