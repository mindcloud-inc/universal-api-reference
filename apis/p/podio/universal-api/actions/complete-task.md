# Podio: Complete Task

Marks an existing task complete in Podio.

```
PUT https://connect.mindcloud.co/v1/universal/podio/latest/actions/complete-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Podio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/podio/latest/actions/complete-task" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "taskId": "12345"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/podio/latest/actions/complete-task', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "taskId": "12345"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `taskId` | string | yes | The ID of the task to complete. Example: `12345`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `hook` | boolean | no | Run Podio hooks for the change. |
| `silent` | boolean | no | Suppress stream bumping and notifications for the completion. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "recurringTaskId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `recurringTaskId` | number |  |

## Native endpoint

Through the native Podio API, this operation is `POST /task/:task_id/complete` (base URL `https://api.podio.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/complete-task.md) for the provider-specific parameters and requirements.

