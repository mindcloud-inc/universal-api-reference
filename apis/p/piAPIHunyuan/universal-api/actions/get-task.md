# PiAPI/Hunyuan: Get Task



```
GET https://connect.mindcloud.co/v1/universal/piAPIHunyuan/latest/actions/get-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PiAPI/Hunyuan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/piAPIHunyuan/latest/actions/get-task?connectionId=$CONNECTION_ID&taskId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "taskId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/piAPIHunyuan/latest/actions/get-task?${params}`, {
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
| `taskId` | string | yes | PiAPI task identifier returned when a Hunyuan task is created. |

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
| `status` | string | Current task status |
| `taskId` | string | PiAPI task identifier |

## Native endpoint

Through the native PiAPI/Hunyuan API, this operation is `GET /api/v1/task/:taskId` (base URL `https://api.piapi.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-task.md) for the provider-specific parameters and requirements.

