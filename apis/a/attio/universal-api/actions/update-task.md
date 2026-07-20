# Attio: Update Task

Updates a task in Attio.

```
PUT https://connect.mindcloud.co/v1/universal/attio/latest/actions/update-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Attio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/attio/latest/actions/update-task" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "task_id": "649e34f4-c39a-4f4d-99ef-48a36bef8f04"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/attio/latest/actions/update-task', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "task_id": "649e34f4-c39a-4f4d-99ef-48a36bef8f04"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `task_id` | string | yes | The ID of the task to update. Example: `649e34f4-c39a-4f4d-99ef-48a36bef8f04`. |
| `deadlineAt` | string | no | Optional deadline for the task. Enter an ISO 8601 timestamp; if omitted, the existing deadline is unchanged. Example: `2023-01-01T15:00:00.000Z`. |
| `isCompleted` | boolean | no | Set whether the task is completed. Leave blank to keep the current completion state. |
| `linkedRecords[]` | array<string> | no | Optional list of email addresses or domains to link to the task. Provide an empty array to clear linked records. Example: `[object Object]`. |
| `assigneeId` | string<string> | no | Optional workspace member ID to assign to the task. Leave blank to keep the current assignees; use the string null to clear them. Example: `[object Object]`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "assignees": [
        {}
      ],
      "contentPlaintext": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "createdByActor": {},
      "deadlineAt": "2026-05-07T12:00:00.000Z",
      "id": {},
      "isCompleted": true,
      "linkedRecords": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `assignees` | array<object> | Task assignees. |
| `contentPlaintext` | string | Plaintext task content. |
| `createdAt` | date | When the task was created. |
| `createdByActor` | object | Actor that created the task. |
| `deadlineAt` | date | Task deadline timestamp, when set. |
| `id` | object | Task identifier payload containing workspace and task ids. |
| `isCompleted` | boolean | Whether the task is completed. |
| `linkedRecords` | array<object> | Records linked to the task. |

## Native endpoint

Through the native Attio API, this operation is `PATCH /v2/tasks/:task_id` (base URL `https://api.attio.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-task.md) for the provider-specific parameters and requirements.

