# Clientary: Create Task

Creates a new task in Clientary.

```
POST https://connect.mindcloud.co/v1/universal/clientary/latest/actions/create-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Clientary `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/clientary/latest/actions/create-task" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "task.title": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/clientary/latest/actions/create-task', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "task.title": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `task.assigneeId` | number | no | Optionally assign the task to a staff member. |
| `task.projectId` | number | no | Optionally assign the task to a project. |
| `task.title` | string | yes | The task title. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "assigneeId": 1,
      "budget": 1,
      "budgetType": "string",
      "clientId": 1,
      "comments": [
        {}
      ],
      "complete": true,
      "completedAt": "2026-05-07T12:00:00.000Z",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "dueDate": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "isTemplateTask": true,
      "projectId": 1,
      "startDate": "2026-05-07T12:00:00.000Z",
      "taskGroupId": 1,
      "title": "string",
      "totalCost": 1,
      "totalHours": 1,
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "userId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `assigneeId` | number |  |
| `budget` | number |  |
| `budgetType` | string |  |
| `clientId` | number |  |
| `comments` | array<object> |  |
| `complete` | boolean |  |
| `completedAt` | date |  |
| `createdAt` | date |  |
| `description` | string |  |
| `dueDate` | date |  |
| `id` | number |  |
| `isTemplateTask` | boolean |  |
| `projectId` | number |  |
| `startDate` | date |  |
| `taskGroupId` | number |  |
| `title` | string |  |
| `totalCost` | number |  |
| `totalHours` | number |  |
| `updatedAt` | date |  |
| `userId` | number |  |

## Native endpoint

Through the native Clientary API, this operation is `POST /tasks` (base URL `https://{{credentials.subdomain}}.clientary.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-task.md) for the provider-specific parameters and requirements.

