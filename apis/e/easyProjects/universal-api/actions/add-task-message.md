# Easy Projects: Add Task Message

Creates a new message on an Easy Projects task.

```
POST https://connect.mindcloud.co/v1/universal/easyProjects/latest/actions/add-task-message
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Easy Projects `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/easyProjects/latest/actions/add-task-message" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "123",
  "model": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/easyProjects/latest/actions/add-task-message', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "123",
    "model": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | Birdview task ID. Example: `123`. |
| `model` | object | yes | New task message model. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": 1,
      "messageText": "string",
      "postDate": "2026-05-07T12:00:00.000Z",
      "projectId": 1,
      "taskId": 1,
      "user": {},
      "userId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number |  |
| `messageText` | string |  |
| `postDate` | date |  |
| `projectId` | number |  |
| `taskId` | number |  |
| `user` | object |  |
| `userId` | number |  |

## Native endpoint

Through the native Easy Projects API, this operation is `POST /api/v1/tasks/:id/messages` (base URL `https://api.go.easyprojects.net/api/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-task-message.md) for the provider-specific parameters and requirements.

