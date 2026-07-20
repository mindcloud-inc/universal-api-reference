# Higgsfield AI: Submit Generation Request

Submits a generation request to Higgsfield AI.

```
POST https://connect.mindcloud.co/v1/universal/higgsfieldAI/latest/actions/submit-generation-request
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Higgsfield AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/higgsfieldAI/latest/actions/submit-generation-request" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "modelId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/higgsfieldAI/latest/actions/submit-generation-request', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "modelId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `modelId` | string | yes | Higgsfield model identifier, for example higgsfield-ai/soul/standard. |
| `prompt` | string | no | Text prompt or motion prompt sent to the selected model. |
| `aspectRatio` | string | no | Generation aspect ratio, for example 16:9. |
| `resolution` | string | no | Generation resolution, for example 720p or 2K. |
| `imageUrl` | string | no | Source image URL for image-to-video or image-editing models. |
| `duration` | number | no | Requested video duration in seconds when supported by the model. |
| `cameraFixed` | boolean | no | Whether the camera should remain fixed when supported by the model. Default: `false`. |

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
      "status_url": "https://example.com",
      "video": {}
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
| `video` | object |  |

## Native endpoint

Through the native Higgsfield AI API, this operation is `POST /{modelId}` (base URL `https://platform.higgsfield.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/submit-generation-request.md) for the provider-specific parameters and requirements.

