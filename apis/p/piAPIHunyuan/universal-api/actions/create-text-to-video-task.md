# PiAPI/Hunyuan: Create Text to Video Task



```
POST https://connect.mindcloud.co/v1/universal/piAPIHunyuan/latest/actions/create-text-to-video-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PiAPI/Hunyuan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/piAPIHunyuan/latest/actions/create-text-to-video-task" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "input.prompt": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/piAPIHunyuan/latest/actions/create-text-to-video-task', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "input.prompt": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `input.prompt` | string | yes |  |
| `input.aspect_ratio` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "output": {},
      "status": "string",
      "taskId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `output` | object | Task output payload when available |
| `status` | string | Initial task status |
| `taskId` | string | Created PiAPI task identifier |

## Native endpoint

Through the native PiAPI/Hunyuan API, this operation is `POST /api/v1/task` (base URL `https://api.piapi.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-text-to-video-task.md) for the provider-specific parameters and requirements.

