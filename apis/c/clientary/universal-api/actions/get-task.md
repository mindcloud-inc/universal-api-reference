# Clientary: Get Task

Retrieves a task from Clientary by task ID.

```
GET https://connect.mindcloud.co/v1/universal/clientary/latest/actions/get-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Clientary `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/clientary/latest/actions/get-task?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/clientary/latest/actions/get-task?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | The Clientary task ID. |

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

Through the native Clientary API, this operation is `GET /tasks/:id` (base URL `https://{{credentials.subdomain}}.clientary.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-task.md) for the provider-specific parameters and requirements.

