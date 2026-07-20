# 88stacks Image Generator: Create Image

Creates images in 88stacks Image Generator from a prompt.

```
POST https://connect.mindcloud.co/v1/universal/stacksImageGenerator/latest/actions/create-image
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a 88stacks Image Generator `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/stacksImageGenerator/latest/actions/create-image" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "prompt": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/stacksImageGenerator/latest/actions/create-image', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "prompt": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `prompt` | string | yes | Prompt text to generate images from. |
| `modelId` | string | no | Model ID to generate images with. |
| `numImages` | number | no | Number of images to create per prompt. Default 4, max 8. |
| `imageUrl` | string | no | Public image URL to use as the source image. |
| `callback` | string | no | Webhook URL to call when image generation completes. |
| `key` | string | no | Optional key used for easier content lookups. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "key": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `key` | string |  |

## Native endpoint

Through the native 88stacks Image Generator API, this operation is `POST /api/v1/invokes` (base URL `https://api.88stacks.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-image.md) for the provider-specific parameters and requirements.

