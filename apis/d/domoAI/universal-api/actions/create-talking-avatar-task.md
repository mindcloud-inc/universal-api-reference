# DomoAI: Create Talking Avatar Task

Creates a new talking avatar task in DomoAI.

```
POST https://connect.mindcloud.co/v1/universal/domoAI/latest/actions/create-talking-avatar-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DomoAI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/domoAI/latest/actions/create-talking-avatar-task" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "audio.domoaiUri": "string",
  "seconds": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/domoAI/latest/actions/create-talking-avatar-task', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "audio.domoaiUri": "string",
    "seconds": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `audio.domoaiUri` | string | yes | A domoai_uri for the driving audio file. |
| `image.domoaiUri` | string | no | Optional domoai_uri for the avatar source image. |
| `video.domoaiUri` | string | no | Optional domoai_uri for the avatar source video. |
| `seconds` | number | yes | Output video duration in seconds. |
| `prompt` | string | no | Optional prompt for generation guidance. |
| `model` | list | no | The DomoAI talking-avatar model version. One of: `talking-avatar-v1`. Default: `talking-avatar-v1`. |
| `aspectRatio` | list | no | Output video aspect ratio. One of: `16:9`, `1:1`, `3:4`, `4:3`, `9:16`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `audio.bytesBase64Encoded` | string | no | Base64-encoded audio bytes. |
| `image.bytesBase64Encoded` | string | no | Optional base64-encoded avatar source image bytes. |
| `video.bytesBase64Encoded` | string | no | Optional base64-encoded avatar source video bytes. |
| `callbackUrl` | string | no | Optional URL that DomoAI should notify when task status changes. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native DomoAI API returns.

## Native endpoint

Through the native DomoAI API, this operation is `POST /v1/video/talking-avatar` (base URL `https://api.domoai.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-talking-avatar-task.md) for the provider-specific parameters and requirements.

