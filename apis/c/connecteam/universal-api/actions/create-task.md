# Connecteam: Create Task

Create quick task for specified users by their ID, detailing information such as title, due date and description. Attachments for the quick task must first be uploaded via the attachments endpoint.

```
POST https://connect.mindcloud.co/v1/universal/connecteam/latest/actions/create-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Connecteam `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/connecteam/latest/actions/create-task" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "taskBoardId": "string",
  "userIds[]": [
    1
  ],
  "status": "string",
  "title": "string",
  "subTasks[].title": "string",
  "description.content": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/connecteam/latest/actions/create-task', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "taskBoardId": "string",
    "userIds[]": [1],
    "status": "string",
    "title": "string",
    "subTasks[].title": "string",
    "description.content": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
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
| `description.content` | string | yes |  |
| `description.attachments[]` | array<object> | no |  |
| `description.attachments[].fileId` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "description": {
        "content": "string"
      },
      "id": "string",
      "isArchived": true,
      "status": "string",
      "subTasks": [
        {
          "id": "string",
          "isCompleted": true,
          "title": "string"
        }
      ],
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
| `description.content` | string |  |
| `id` | string |  |
| `isArchived` | boolean |  |
| `status` | string |  |
| `subTasks[].id` | string |  |
| `subTasks[].isCompleted` | boolean |  |
| `subTasks[].title` | string |  |
| `title` | string |  |
| `type` | string |  |
| `userIds[]` | number |  |

## Native endpoint

Through the native Connecteam API, this operation is `POST /tasks/v1/taskboards/:taskBoardId/tasks` (base URL `https://api.connecteam.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-task.md) for the provider-specific parameters and requirements.

