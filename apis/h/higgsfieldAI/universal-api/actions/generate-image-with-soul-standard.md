# Higgsfield AI: Generate Image with Soul Standard

Creates an image with Soul Standard in Higgsfield AI.

```
POST https://connect.mindcloud.co/v1/universal/higgsfieldAI/latest/actions/generate-image-with-soul-standard
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Higgsfield AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/higgsfieldAI/latest/actions/generate-image-with-soul-standard" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "prompt": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/higgsfieldAI/latest/actions/generate-image-with-soul-standard', {
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
| `prompt` | string | yes | Text prompt describing the image to generate. |
| `aspectRatio` | string | no | Generation aspect ratio, for example 16:9. |
| `resolution` | string | no | Generation resolution, for example 720p. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `webhookUrl` | string | no | Optional public webhook URL for final generation status notifications. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "cancel_url": "https://example.com",
      "error": "string",
      "images": [
        {}
      ],
      "request_id": "string",
      "status": "string",
      "status_url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `cancel_url` | string |  |
| `error` | string |  |
| `images` | array<object> |  |
| `request_id` | string |  |
| `status` | string |  |
| `status_url` | string |  |

## Native endpoint

Through the native Higgsfield AI API, this operation is `POST /higgsfield-ai/soul/standard` (base URL `https://platform.higgsfield.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/generate-image-with-soul-standard.md) for the provider-specific parameters and requirements.

