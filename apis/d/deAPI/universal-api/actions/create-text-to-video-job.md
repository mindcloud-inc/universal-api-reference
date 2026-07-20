# deAPI: Create Text-to-Video Job

Creates a text-to-video job in deAPI.

```
POST https://connect.mindcloud.co/v1/universal/deAPI/latest/actions/create-text-to-video-job
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a deAPI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/deAPI/latest/actions/create-text-to-video-job" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/deAPI/latest/actions/create-text-to-video-job', {
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
| `fps` | string | no | Frames per second for the generated video. |
| `frames` | string | no | Number of frames to generate. |
| `guidance` | string | no | Guidance scale for generation. |
| `height` | string | no | Video height in pixels. |
| `model` | string | no | Video model slug from List Models. |
| `negativePrompt` | string | no | Elements to avoid in the generated video. |
| `prompt` | string | no | Main prompt for video generation. |
| `seed` | string | no | Random seed for generation. |
| `steps` | string | no | Number of inference steps. |
| `width` | string | no | Video width in pixels. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native deAPI API returns.

## Native endpoint

Through the native deAPI API, this operation is `POST /api/v1/client/txt2video` (base URL `https://api.deapi.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-text-to-video-job.md) for the provider-specific parameters and requirements.

