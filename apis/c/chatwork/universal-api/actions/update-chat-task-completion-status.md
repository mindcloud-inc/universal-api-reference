# Chatwork: Update Chat Task Completion Status



```
PUT https://connect.mindcloud.co/v1/universal/chatwork/latest/actions/update-chat-task-completion-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Chatwork `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/chatwork/latest/actions/update-chat-task-completion-status" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "roomId": "123456789",
  "taskId": "123456789",
  "status": "done"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/chatwork/latest/actions/update-chat-task-completion-status', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "roomId": "123456789",
    "taskId": "123456789",
    "status": "done"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `roomId` | number | yes | Room ID. Example: `123456789`. |
| `taskId` | number | yes | Task ID. Example: `123456789`. |
| `status` | list<string> | yes | Task status value. Use open to reopen a task or done to complete it. One of: `done`, `open`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "taskId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `taskId` | string |  |

## Native endpoint

Through the native Chatwork API, this operation is `PUT /rooms/:room_id/tasks/:task_id/status` (base URL `https://api.chatwork.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-chat-task-completion-status.md) for the provider-specific parameters and requirements.

