# Higgsfield AI: Generate Video with Kling 2.1 Pro

Creates a video with Kling 2.1 Pro in Higgsfield AI.

```
POST https://connect.mindcloud.co/v1/universal/higgsfieldAI/latest/actions/generate-video-with-kling21-pro
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Higgsfield AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/higgsfieldAI/latest/actions/generate-video-with-kling21-pro" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "imageUrl": "https://example.com",
  "prompt": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/higgsfieldAI/latest/actions/generate-video-with-kling21-pro', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "imageUrl": "https://example.com",
    "prompt": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `imageUrl` | string | yes | Source image URL to animate into a video. |
| `prompt` | string | yes | Motion prompt describing the video animation. |

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
| `request_id` | string |  |
| `status` | string |  |
| `status_url` | string |  |
| `video` | object |  |

## Native endpoint

Through the native Higgsfield AI API, this operation is `POST /kling-video/v2.1/pro/image-to-video` (base URL `https://platform.higgsfield.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/generate-video-with-kling21-pro.md) for the provider-specific parameters and requirements.

