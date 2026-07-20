# Checkvist: Delete Task Note

Deletes a task note from Checkvist.

```
DELETE https://connect.mindcloud.co/v1/universal/checkvist/latest/actions/delete-task-note
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Checkvist `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/checkvist/latest/actions/delete-task-note?connectionId=$CONNECTION_ID&checklistId=1&noteId=1&taskId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "checklistId": "1",
  "noteId": "1",
  "taskId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/checkvist/latest/actions/delete-task-note?${params}`, {
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
| `checklistId` | number | yes | The checklist ID. |
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

Through the native Checkvist API, this operation is `DELETE /checklists/:checklistId/tasks/:taskId/comments/:noteId.json` (base URL `https://checkvist.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-task-note.md) for the provider-specific parameters and requirements.

