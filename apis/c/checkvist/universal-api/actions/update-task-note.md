# Checkvist: Update Task Note

Updates a task note in Checkvist.

```
PUT https://connect.mindcloud.co/v1/universal/checkvist/latest/actions/update-task-note
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Checkvist `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/checkvist/latest/actions/update-task-note" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "checklistId": 1,
  "comment": "string",
  "noteId": 1,
  "taskId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/checkvist/latest/actions/update-task-note', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "checklistId": 1,
    "comment": "string",
    "noteId": 1,
    "taskId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `checklistId` | number | yes | The checklist ID. |
| `comment` | string | yes | The updated note text. |
| `noteId` | number | yes | The note ID. |
| `taskId` | number | yes | The task ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "comment": "string",
      "createdAt": "string",
      "emailMd5": "ava@example.com",
      "id": 1,
      "taskId": 1,
      "updatedAt": "string",
      "userId": 1,
      "username": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `comment` | string |  |
| `createdAt` | string |  |
| `emailMd5` | string |  |
| `id` | number |  |
| `taskId` | number |  |
| `updatedAt` | string |  |
| `userId` | number |  |
| `username` | string |  |

## Native endpoint

Through the native Checkvist API, this operation is `PUT /checklists/:checklistId/tasks/:taskId/comments/:noteId.json` (base URL `https://checkvist.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-task-note.md) for the provider-specific parameters and requirements.

