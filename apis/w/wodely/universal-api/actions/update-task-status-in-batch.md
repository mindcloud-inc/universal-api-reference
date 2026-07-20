# Wodely: Update Task Status in Batch



```
PUT https://connect.mindcloud.co/v1/universal/wodely/latest/actions/update-task-status-in-batch
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Wodely `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/wodely/latest/actions/update-task-status-in-batch" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "updates[].taskGuid": "DD2A6408A6",
  "updates[].statusId": "10"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/wodely/latest/actions/update-task-status-in-batch', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "updates[].taskGuid": "DD2A6408A6",
    "updates[].statusId": "10"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `updates[].taskGuid` | string | yes | Task Id. Example: `DD2A6408A6`. |
| `updates[].statusId` | number | yes | 10:Unassigned 15:Assigning 20:Assigned 25:Processed 28:Loaded 30:Transit 40:Arrived 45:Awaiting Collection 50:Completed 51:Failed 52:Returned 90:Cancelled. Example: `10`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": "string",
      "message": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | string |  |
| `message` | string |  |
| `success` | boolean |  |

## Native endpoint

Through the native Wodely API, this operation is `POST /v2/tasks/status` (base URL `https://api.wodely.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-task-status-in-batch.md) for the provider-specific parameters and requirements.

