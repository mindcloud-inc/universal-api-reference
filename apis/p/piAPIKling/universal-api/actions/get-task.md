# PiAPI/Kling: Get Task



```
GET https://connect.mindcloud.co/v1/universal/piAPIKling/latest/actions/get-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PiAPI/Kling `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/piAPIKling/latest/actions/get-task?connectionId=$CONNECTION_ID&taskId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "taskId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/piAPIKling/latest/actions/get-task?${params}`, {
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
| `taskId` | string | yes | The PiAPI task ID to retrieve. |

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

Through the native PiAPI/Kling API, this operation is `GET /api/v1/task/:task_id` (base URL `https://api.piapi.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-task.md) for the provider-specific parameters and requirements.

