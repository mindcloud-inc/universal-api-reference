# PiAPI/Veo: Get Task

Retrieves a Veo task from PiAPI/Veo by ID.

```
GET https://connect.mindcloud.co/v1/universal/piAPIVeo/latest/actions/get-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PiAPI/Veo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/piAPIVeo/latest/actions/get-task?connectionId=$CONNECTION_ID&taskId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "taskId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/piAPIVeo/latest/actions/get-task?${params}`, {
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
| `taskId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": 1,
      "data": {
        "status": "string",
        "task_id": "string"
      },
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | number |  |
| `data` | object |  |
| `data.status` | string |  |
| `data.task_id` | string |  |
| `message` | string |  |

## Native endpoint

Through the native PiAPI/Veo API, this operation is `GET /api/v1/task/:taskId` (base URL `https://api.piapi.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-task.md) for the provider-specific parameters and requirements.

