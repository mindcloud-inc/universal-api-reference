# Todoist: Update Task

Updates an existing task in Todoist.

```
PUT https://connect.mindcloud.co/v1/universal/todoist/latest/actions/update-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Todoist `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/todoist/latest/actions/update-task" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "taskId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/todoist/latest/actions/update-task', {
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
| `taskId` | string | yes |  |
| `content` | string | no |  |
| `description` | string | no |  |
| `labels` | list<string> | no |  |
| `priority` | number | no |  |
| `dueString` | string | no |  |
| `dueDate` | date | no |  |
| `dueDatetime` | date | no |  |
| `dueLang` | string | no |  |
| `duration` | number | no |  |
| `durationUnit` | string | no |  |
| `deadlineDate` | date | no |  |

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
      "isDeleted": true,
      "labels": [
        "string"
      ],
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
| `addedAt` | date |  |
| `checked` | boolean |  |
| `content` | string |  |
| `description` | string |  |
| `due` | object |  |
| `id` | string |  |
| `isDeleted` | boolean |  |
| `labels` | array<string> |  |
| `parentId` | string |  |
| `priority` | number |  |
| `projectId` | string |  |
| `sectionId` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Todoist API, this operation is `POST /api/v1/tasks/:task_id` (base URL `https://api.todoist.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-task.md) for the provider-specific parameters and requirements.

