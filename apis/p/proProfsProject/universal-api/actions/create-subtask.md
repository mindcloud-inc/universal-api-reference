# ProProfs Project: Create Subtask

Creates a new subtask in ProProfs Project.

```
POST https://connect.mindcloud.co/v1/universal/proProfsProject/latest/actions/create-subtask
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ProProfs Project `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/proProfsProject/latest/actions/create-subtask" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "subtaskName": "Ava Chen",
  "taskId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/proProfsProject/latest/actions/create-subtask', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "subtaskName": "Ava Chen",
    "taskId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `subtaskName` | string | yes | The subtask name. |
| `taskId` | string | yes | The parent task ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "active": "string",
      "archived": "string",
      "billableHours": 1,
      "billed": 1,
      "color": "string",
      "completed": "string",
      "dateCompleted": "string",
      "dateCreated": "string",
      "dateModified": "string",
      "description": "string",
      "dueDate": "string",
      "estimatedCost": "string",
      "estimatedHours": "string",
      "fixedPrice": "string",
      "hourlyRate": "https://example.com",
      "important": "string",
      "notes": "string",
      "notifications": "string",
      "ongoing": "string",
      "price": "string",
      "progress": "string",
      "projectId": "string",
      "projectName": "Ava Chen",
      "recurring": "string",
      "startDate": "string",
      "subtaskId": "string",
      "subtaskName": "Ava Chen",
      "subtaskOrder": "string",
      "tags": "string",
      "taskId": "string",
      "taskName": "Ava Chen",
      "trackedSeconds": "string",
      "userId": "string",
      "users": [
        {
          "userId": "string",
          "userName": "Ava Chen"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | string |  |
| `archived` | string |  |
| `billableHours` | number |  |
| `billed` | number |  |
| `color` | string |  |
| `completed` | string |  |
| `dateCompleted` | string |  |
| `dateCreated` | string |  |
| `dateModified` | string |  |
| `description` | string |  |
| `dueDate` | string |  |
| `estimatedCost` | string |  |
| `estimatedHours` | string |  |
| `fixedPrice` | string |  |
| `hourlyRate` | string |  |
| `important` | string |  |
| `notes` | string |  |
| `notifications` | string |  |
| `ongoing` | string |  |
| `price` | string |  |
| `progress` | string |  |
| `projectId` | string |  |
| `projectName` | string |  |
| `recurring` | string |  |
| `startDate` | string |  |
| `subtaskId` | string |  |
| `subtaskName` | string |  |
| `subtaskOrder` | string |  |
| `tags` | string |  |
| `taskId` | string |  |
| `taskName` | string |  |
| `trackedSeconds` | string |  |
| `userId` | string |  |
| `users[].userId` | string |  |
| `users[].userName` | string |  |

## Native endpoint

Through the native ProProfs Project API, this operation is `POST /subtasks/{{task_id}}` (base URL `https://api.projectbubble.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-subtask.md) for the provider-specific parameters and requirements.

