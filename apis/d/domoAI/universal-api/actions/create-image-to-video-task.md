# DomoAI: Create Image to Video Task

Creates a new image-to-video task in DomoAI.

```
POST https://connect.mindcloud.co/v1/universal/domoAI/latest/actions/create-image-to-video-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DomoAI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/domoAI/latest/actions/create-image-to-video-task" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "model": "animate-2.4-faster",
  "image.domoaiUri": "string",
  "seconds": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/domoAI/latest/actions/create-image-to-video-task', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "model": "animate-2.4-faster",
    "image.domoaiUri": "string",
    "seconds": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `model` | list | yes | The DomoAI image-to-video model version. One of: `animate-2.4-advanced`, `animate-2.4-faster`. Default: `animate-2.4-faster`. |
| `image.domoaiUri` | string | yes | A domoai_uri from the Upload File action. |
| `seconds` | number | yes | Output video duration in seconds. |
| `prompt` | string | no | Optional text prompt describing the video style or motion. |
| `aspectRatio` | list | no | Output video aspect ratio. One of: `16:9`, `1:1`, `3:4`, `4:3`, `9:16`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `image.bytesBase64Encoded` | string | no | Base64-encoded image bytes. |
| `callbackUrl` | string | no | Optional URL that DomoAI should notify when task status changes. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native DomoAI API returns.

## Native endpoint

Through the native DomoAI API, this operation is `POST /v1/video/image2video` (base URL `https://api.domoai.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-image-to-video-task.md) for the provider-specific parameters and requirements.

