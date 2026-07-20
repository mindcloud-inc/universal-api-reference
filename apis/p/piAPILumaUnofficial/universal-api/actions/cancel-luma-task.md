# PiAPI/Luma (unofficial): Cancel Luma Task

Cancels an existing Luma task in PiAPI.

```
DELETE https://connect.mindcloud.co/v1/universal/piAPILumaUnofficial/latest/actions/cancel-luma-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PiAPI/Luma (unofficial) `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/piAPILumaUnofficial/latest/actions/cancel-luma-task?connectionId=$CONNECTION_ID&taskId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "taskId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/piAPILumaUnofficial/latest/actions/cancel-luma-task?${params}`, {
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
| `taskId` | string | yes | Pending Luma task identifier to cancel. |

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
| `code` | number |  |
| `message` | string |  |

## Native endpoint

Through the native PiAPI/Luma (unofficial) API, this operation is `DELETE /api/v1/task/:task_id` (base URL `https://api.piapi.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/cancel-luma-task.md) for the provider-specific parameters and requirements.

