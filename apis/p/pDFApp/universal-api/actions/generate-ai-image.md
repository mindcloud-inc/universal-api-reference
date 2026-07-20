# PDF-app: Generate AI Image

Creates an AI-generated image in PDF-app.

```
POST https://connect.mindcloud.co/v1/universal/pDFApp/latest/actions/generate-ai-image
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PDF-app `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/pDFApp/latest/actions/generate-ai-image" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pDFApp/latest/actions/generate-ai-image', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `prompt` | string | no | Natural-language prompt describing the image to generate. Example: `A cozy reading nook lit by sunset, cinematic illustration`. |
| `fileUrls[]` | array<string> | no | Optional conditioning image URLs to guide generation. Example: `https://example.com/reference-image.png`. |
| `numberOfImages` | number | no | How many output images to generate. Example: `1`. |
| `width` | number | no | Output image width in pixels. Example: `1024`. |
| `height` | number | no | Output image height in pixels. Example: `1024`. |
| `cfgScale` | number | no | Guidance scale controlling prompt adherence versus creativity. Example: `7.5`. |
| `seed` | number | no | Seed used for reproducible image generation. Example: `0`. |
| `quality` | string | no | Generation quality level: standard or premium. Example: `standard`. |
| `async` | boolean | no | Whether to run the image generation asynchronously. Default: `false`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native PDF-app API returns.

## Native endpoint

Through the native PDF-app API, this operation is `POST /ai_img_generator` (base URL `https://api.pdf-app.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/generate-ai-image.md) for the provider-specific parameters and requirements.

