# DomoAI: Create Template to Video Task

Creates a new template-to-video task in DomoAI.

```
POST https://connect.mindcloud.co/v1/universal/domoAI/latest/actions/create-template-to-video-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DomoAI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/domoAI/latest/actions/create-template-to-video-task" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "template": "360_view",
  "images[].domoaiUri": "string",
  "seconds": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/domoAI/latest/actions/create-template-to-video-task', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "template": "360_view",
    "images[].domoaiUri": "string",
    "seconds": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `template` | list | yes | The DomoAI template preset to use. One of: `360_view`, `crane_up`, `french_kiss`, `groove_dance`, `hug`, `kiss`, `kissing_screen`, `looping_animation`, `zoom_in`, `zoom_out`. |
| `images[].domoaiUri` | string | yes | A domoai_uri from the Upload File action. |
| `seconds` | number | yes | Output video duration in seconds. |
| `prompt` | string | no | Optional prompt to guide the template animation. |
| `aspectRatio` | list | no | Output video aspect ratio. One of: `16:9`, `1:1`, `3:4`, `4:3`, `9:16`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `images[].bytesBase64Encoded` | string | no | Base64-encoded image bytes for the template input image. |
| `callbackUrl` | string | no | Optional URL that DomoAI should notify when task status changes. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native DomoAI API returns.

## Native endpoint

Through the native DomoAI API, this operation is `POST /v1/video/template2video` (base URL `https://api.domoai.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-template-to-video-task.md) for the provider-specific parameters and requirements.

