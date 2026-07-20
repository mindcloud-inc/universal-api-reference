# DomoAI: Create Text to Video Task

Creates a new text-to-video task in DomoAI.

```
POST https://connect.mindcloud.co/v1/universal/domoAI/latest/actions/create-text-to-video-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DomoAI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/domoAI/latest/actions/create-text-to-video-task" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "prompt": "string",
  "seconds": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/domoAI/latest/actions/create-text-to-video-task', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "prompt": "string",
    "seconds": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `prompt` | string | yes | The text prompt that describes the video to generate. |
| `seconds` | number | yes | Output video duration in seconds. |
| `model` | list | no | The DomoAI text-to-video model version. One of: `t2v-2.4-advanced`, `t2v-2.4-faster`. Default: `t2v-2.4-faster`. |
| `style` | list | no | Optional visual style preset. One of: `90s_style`, `cartoon_game`, `flat_color_anime`, `japanese_anime`, `pixel`, `realistic`. |
| `aspectRatio` | list | no | Output video aspect ratio. One of: `16:9`, `1:1`, `3:4`, `4:3`, `9:16`. Default: `1:1`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `callbackUrl` | string | no | Optional URL that DomoAI should notify when task status changes. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native DomoAI API returns.

## Native endpoint

Through the native DomoAI API, this operation is `POST /v1/video/text2video` (base URL `https://api.domoai.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-text-to-video-task.md) for the provider-specific parameters and requirements.

