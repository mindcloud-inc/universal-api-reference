# ProProfs Project: Get Subtask

Retrieves a subtask from ProProfs Project.

```
GET https://connect.mindcloud.co/v1/universal/proProfsProject/latest/actions/get-subtask
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ProProfs Project `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/proProfsProject/latest/actions/get-subtask?connectionId=$CONNECTION_ID&subtaskId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "subtaskId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/proProfsProject/latest/actions/get-subtask?${params}`, {
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
| `subtaskId` | string | yes | The subtask ID to fetch. |

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

Through the native ProProfs Project API, this operation is `GET /subtasks/{{subtask_id}}` (base URL `https://api.projectbubble.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-subtask.md) for the provider-specific parameters and requirements.

