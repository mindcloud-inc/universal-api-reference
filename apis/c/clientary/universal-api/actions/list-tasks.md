# Clientary: List Tasks

Retrieves tasks from your Clientary account.

```
GET https://connect.mindcloud.co/v1/universal/clientary/latest/actions/list-tasks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Clientary `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/clientary/latest/actions/list-tasks?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/clientary/latest/actions/list-tasks?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



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

Through the native Clientary API, this operation is `GET /tasks` (base URL `https://{{credentials.subdomain}}.clientary.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-tasks.md) for the provider-specific parameters and requirements.

