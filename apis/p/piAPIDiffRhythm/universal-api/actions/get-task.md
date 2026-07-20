# PiAPI/DiffRhythm: Get Task

Retrieves a DiffRhythm task from PiAPI/DiffRhythm.

```
GET https://connect.mindcloud.co/v1/universal/piAPIDiffRhythm/latest/actions/get-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PiAPI/DiffRhythm `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/piAPIDiffRhythm/latest/actions/get-task?connectionId=$CONNECTION_ID&taskId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "taskId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/piAPIDiffRhythm/latest/actions/get-task?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `taskId` | string | yes | The PiAPI task ID returned when you created the DiffRhythm generation task. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "config": {
        "serviceMode": "string",
        "webhookConfig": {
          "endpoint": "string",
          "secret": "string"
        }
      },
      "detail": {},
      "error": {
        "code": 1,
        "detail": {},
        "message": "string",
        "rawMessage": "string"
      },
      "input": {
        "lyrics": "string",
        "styleAudio": "string",
        "stylePrompt": "string"
      },
      "logs": [
        {}
      ],
      "meta": {
        "createdAt": "string",
        "endedAt": "string",
        "isUsingPrivatePool": true,
        "startedAt": "string",
        "usage": {
          "consume": 1,
          "frozen": 1,
          "type": "string"
        }
      },
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
| `config.serviceMode` | string |  |
| `config.webhookConfig.endpoint` | string |  |
| `config.webhookConfig.secret` | string |  |
| `detail` | object |  |
| `error.code` | number |  |
| `error.detail` | object |  |
| `error.message` | string |  |
| `error.rawMessage` | string |  |
| `input.lyrics` | string |  |
| `input.styleAudio` | string |  |
| `input.stylePrompt` | string |  |
| `logs` | array<object> |  |
| `meta.createdAt` | string |  |
| `meta.endedAt` | string |  |
| `meta.isUsingPrivatePool` | boolean |  |
| `meta.startedAt` | string |  |
| `meta.usage.consume` | number |  |
| `meta.usage.frozen` | number |  |
| `meta.usage.type` | string |  |
| `model` | string |  |
| `output` | object |  |
| `status` | string |  |
| `taskId` | string |  |
| `taskType` | string |  |

## Native endpoint

Through the native PiAPI/DiffRhythm API, this operation is `GET /api/v1/task/{task_id}` (base URL `https://api.piapi.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-task.md) for the provider-specific parameters and requirements.

