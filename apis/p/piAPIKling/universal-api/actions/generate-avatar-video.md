# PiAPI/Kling: Generate Avatar Video



```
POST https://connect.mindcloud.co/v1/universal/piAPIKling/latest/actions/generate-avatar-video
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PiAPI/Kling `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/piAPIKling/latest/actions/generate-avatar-video" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "input.imageUrl": "https://example.com",
  "input.localDubbingUrl": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/piAPIKling/latest/actions/generate-avatar-video', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "input.imageUrl": "https://example.com",
    "input.localDubbingUrl": "https://example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `input.imageUrl` | string | yes | Source avatar image URL. |
| `input.localDubbingUrl` | string | yes | Audio URL to drive the avatar speech. |
| `input.prompt` | string | no | Optional prompt to guide the avatar delivery. |
| `input.mode` | string | no | Avatar generation mode, such as std or pro. |
| `input.batchSize` | number | no | Number of avatar outputs to request. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "config": {},
      "detail": {},
      "error": {},
      "input": {},
      "logs": [
        {}
      ],
      "meta": {},
      "model": "string",
      "output": {},
      "status": "string",
      "taskId": "string",
      "taskType": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `config` | object | Resolved task configuration. |
| `detail` | object | Provider detail payload when available. |
| `error` | object | Provider error payload. |
| `input` | object | Submitted task input payload. |
| `logs` | array<object> | Task log entries when available. |
| `meta` | object | Task timestamps and usage metadata. |
| `model` | string | Provider model name. |
| `output` | object | Provider output payload. |
| `status` | string | Current task status. |
| `taskId` | string | PiAPI task identifier. |
| `taskType` | string | PiAPI task type. |

## Native endpoint

Through the native PiAPI/Kling API, this operation is `POST /api/v1/task` (base URL `https://api.piapi.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/generate-avatar-video.md) for the provider-specific parameters and requirements.

