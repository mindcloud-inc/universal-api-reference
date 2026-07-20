# TickTick: Complete Task

Marks a task as complete in TickTick.

```
PUT https://connect.mindcloud.co/v1/universal/tickTick/latest/actions/complete-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TickTick `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/tickTick/latest/actions/complete-task" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "projectId": "string",
  "taskId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/tickTick/latest/actions/complete-task', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "projectId": "string",
    "taskId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `projectId` | list<string> | yes | Project identifier |
| `taskId` | string | yes | Task identifier |

## Response

```json
{
  "success": true,
  "data": [
    {
      "projectId": "string",
      "taskId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `projectId` | string |  |
| `taskId` | string |  |

## Native endpoint

Through the native TickTick API, this operation is `POST /open/v1/project/:projectId/task/:taskId/complete` (base URL `https://api.ticktick.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/complete-task.md) for the provider-specific parameters and requirements.

