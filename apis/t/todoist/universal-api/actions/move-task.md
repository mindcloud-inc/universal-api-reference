# Todoist: Move Task

Moves an existing task in Todoist.

```
PUT https://connect.mindcloud.co/v1/universal/todoist/latest/actions/move-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Todoist `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/todoist/latest/actions/move-task" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "taskId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/todoist/latest/actions/move-task', {
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
| `taskId` | string | yes | ID of the task to move |
| `projectId` | string | no | Destination project ID |
| `sectionId` | string | no | Destination section ID |
| `parentId` | string | no | Destination parent task ID |

## Response

```json
{
  "success": true,
  "data": [
    {
      "addedAt": "2026-05-07T12:00:00.000Z",
      "checked": true,
      "content": "string",
      "description": "string",
      "due": {},
      "id": "string",
      "noteCount": 1,
      "parentId": "string",
      "priority": 1,
      "projectId": "string",
      "sectionId": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `addedAt` | date | Task creation timestamp |
| `checked` | boolean | Task completion flag |
| `content` | string | Task content |
| `description` | string | Task description |
| `due` | object | Due information |
| `id` | string | Task ID |
| `noteCount` | number | Number of notes |
| `parentId` | string | Parent task ID |
| `priority` | number | Task priority |
| `projectId` | string | Project ID |
| `sectionId` | string | Section ID |
| `updatedAt` | date | Last update timestamp |

## Native endpoint

Through the native Todoist API, this operation is `POST /api/v1/tasks/:task_id/move` (base URL `https://api.todoist.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/move-task.md) for the provider-specific parameters and requirements.

