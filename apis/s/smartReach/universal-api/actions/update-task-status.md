# SmartReach: Update Task Status

Updates task status in SmartReach.

```
PUT https://connect.mindcloud.co/v1/universal/smartReach/latest/actions/update-task-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SmartReach `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/smartReach/latest/actions/update-task-status" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "taskId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/smartReach/latest/actions/update-task-status', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "taskId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `taskId` | string | yes | Task UUID |
| `dueAt` | number | no | The date-time with respective time-zone of schedule start should be converted to Epoch milliseconds and passed. |
| `statusType` | string | no |  |
| `snoozedTill` | number | no | DateTime until when the task is snoozed.The date-time with respective time-zone of schedule start should be converted to Epoch milliseconds and passed. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "status_type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `status_type` | string |  |

## Native endpoint

Through the native SmartReach API, this operation is `PUT /tasks/:task_id/status` (base URL `https://api.smartreach.io/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-task-status.md) for the provider-specific parameters and requirements.

