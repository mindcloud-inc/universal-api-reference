# Connecteam: Update Task

Update a quick task under a specified task board. Any new attachments will replace the existing ones.

```
PUT https://connect.mindcloud.co/v1/universal/connecteam/latest/actions/update-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Connecteam `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/connecteam/latest/actions/update-task" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "taskId": "string",
  "taskBoardId": "string",
  "userIds[]": [
    1
  ],
  "status": "string",
  "title": "string",
  "subTasks[].title": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/connecteam/latest/actions/update-task', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "taskId": "string",
    "taskBoardId": "string",
    "userIds[]": [1],
    "status": "string",
    "title": "string",
    "subTasks[].title": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `taskId` | string | yes |  |
| `taskBoardId` | string | yes |  |
| `userIds[]` | array<number> | yes |  |
| `status` | string | yes |  |
| `title` | string | yes |  |
| `startTime` | number | no |  |
| `dueDate` | number | no |  |
| `labelIds[]` | array<string> | no |  |
| `type` | string | no |  |
| `isArchived` | boolean | no | Default: `false`. |
| `subTasks[]` | array<object> | no |  |
| `subTasks[].title` | string | yes |  |
| `subTasks[].isCompleted` | boolean | no | Default: `false`. |
| `description` | object | no |  |
| `description.content` | string | no |  |
| `description.attachments[]` | array<object> | no |  |
| `description.attachments[].fileId` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "isArchived": true,
      "status": "string",
      "title": "string",
      "type": "string",
      "userIds": [
        1
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `isArchived` | boolean |  |
| `status` | string |  |
| `title` | string |  |
| `type` | string |  |
| `userIds[]` | number |  |

## Native endpoint

Through the native Connecteam API, this operation is `PUT /tasks/v1/taskboards/:taskBoardId/tasks/:taskId` (base URL `https://api.connecteam.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-task.md) for the provider-specific parameters and requirements.

