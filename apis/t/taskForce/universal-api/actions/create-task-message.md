# TaskForce: Create Task Message

Sends a task message in TaskForce.

```
POST https://connect.mindcloud.co/v1/universal/taskForce/latest/actions/create-task-message
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TaskForce `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/taskForce/latest/actions/create-task-message" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "content": "string",
  "taskId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/taskForce/latest/actions/create-task-message', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "content": "string",
    "taskId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `content` | string | yes | Message text. |
| `taskId` | string | yes | Task identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | object | Created task message payload. |

## Native endpoint

Through the native TaskForce API, this operation is `POST /tasks/:taskId/messages` (base URL `https://www.task-force.app/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-task-message.md) for the provider-specific parameters and requirements.

