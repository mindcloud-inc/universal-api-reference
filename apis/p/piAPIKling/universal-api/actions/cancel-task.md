# PiAPI/Kling: Cancel Task



```
DELETE https://connect.mindcloud.co/v1/universal/piAPIKling/latest/actions/cancel-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PiAPI/Kling `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/piAPIKling/latest/actions/cancel-task?connectionId=$CONNECTION_ID&taskId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "taskId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/piAPIKling/latest/actions/cancel-task?${params}`, {
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
| `taskId` | string | yes | The pending PiAPI task ID to cancel. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": 1,
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | number | PiAPI response code. |
| `message` | string | Provider cancellation result message. |

## Native endpoint

Through the native PiAPI/Kling API, this operation is `DELETE /api/v1/task/:task_id` (base URL `https://api.piapi.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/cancel-task.md) for the provider-specific parameters and requirements.

