# Attio: Create Task

Creates a task in Attio.

```
POST https://connect.mindcloud.co/v1/universal/attio/latest/actions/create-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Attio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/attio/latest/actions/create-task" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "content": "Follow up on current software solutions"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/attio/latest/actions/create-task', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "content": "Follow up on current software solutions"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `content` | string | yes | The text content of the task. Example: `Follow up on current software solutions`. |
| `deadlineAt` | string | no | Optional deadline for the task. Enter an ISO 8601 timestamp; the mapper validates and sends it to Attio only when valid. Example: `2026-05-20T15:00:00.000Z`. |
| `linkedRecords[]` | array<string> | no | Optional list of email addresses or domains to link to the task. Example: `fundstack.com`. |
| `assigneeId` | string<object> | no | Optional workspace member ID to assign to the task. Example: `50cf242c-7fa3-4cad-87d0-75b1af71c57b`. |

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

Through the native Attio API, this operation is `POST /v2/tasks` (base URL `https://api.attio.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-task.md) for the provider-specific parameters and requirements.

