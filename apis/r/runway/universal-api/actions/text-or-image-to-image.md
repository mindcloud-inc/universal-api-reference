# Runway: Text Or Image To Image

Creates an image generation task from text or images in Runway.

```
POST https://connect.mindcloud.co/v1/universal/runway/latest/actions/text-or-image-to-image
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Runway `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/runway/latest/actions/text-or-image-to-image" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "model": "gen4_image_turbo",
  "promptText": "string",
  "ratio": "1024:1024",
  "referenceImages[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/runway/latest/actions/text-or-image-to-image', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "model": "gen4_image_turbo",
    "promptText": "string",
    "ratio": "1024:1024",
    "referenceImages[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `model` | string | yes | Image generation model, such as gen4_image_turbo, gen4_image, or gemini_2.5_flash. Default: `gen4_image_turbo`. |
| `promptText` | string | yes | Detailed text prompt for the image generation. |
| `ratio` | string | yes | Requested output image ratio, such as 1024:1024 or 1280:720. Default: `1024:1024`. |
| `referenceImages[]` | array<object> | yes | One to three reference image objects with uri and optional tag. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "string",
      "error": "string",
      "id": "string",
      "progress": 1,
      "status": "string",
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | string |  |
| `error` | string |  |
| `id` | string |  |
| `progress` | number |  |
| `status` | string |  |
| `updatedAt` | string |  |

## Native endpoint

Through the native Runway API, this operation is `POST /v1/text_to_image` (base URL `https://api.dev.runwayml.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/text-or-image-to-image.md) for the provider-specific parameters and requirements.

