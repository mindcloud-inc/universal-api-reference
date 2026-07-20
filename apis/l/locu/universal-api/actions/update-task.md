# Locu: Update Task

Updates an existing task in Locu.

```
PUT https://connect.mindcloud.co/v1/universal/locu/latest/actions/update-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Locu `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/locu/latest/actions/update-task" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/locu/latest/actions/update-task', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | Task ID |
| `name` | string | no | Task name |
| `description` | string | no | Task description in markdown format |
| `done` | string | no | Set task completion state One of: `0`, `1`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `projectId` | string | no | Project to assign the task to |
| `waiting.reason` | string | no | Reason for marking the task as waiting |
| `keepBreaks` | boolean | no | Preserve extra blank lines as empty paragraphs Default: `true`. |
| `includeHtml` | boolean | no | Include description content as HTML |
| `includeMarkdown` | boolean | no | Include description content as Markdown |
| `includePlainText` | boolean | no | Include description content as plain text |
| `includeJson` | boolean | no | Include description content as structured JSON |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "done": "string",
      "doneAt": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "integrationId": "string",
      "name": "Ava Chen",
      "projectId": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date | Task creation timestamp |
| `done` | string | Task completion state |
| `doneAt` | date | Task completion timestamp |
| `id` | string | Task ID |
| `integrationId` | string | Linked integration ID |
| `name` | string | Task name |
| `projectId` | string | Assigned project ID |
| `type` | string | Task type |

## Native endpoint

Through the native Locu API, this operation is `PATCH /tasks/:id` (base URL `https://api.locu.app/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-task.md) for the provider-specific parameters and requirements.

