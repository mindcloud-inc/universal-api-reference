# Queue: Create Column Task

Creates a new task for a Queue column.

```
POST https://connect.mindcloud.co/v1/universal/queue/latest/actions/create-column-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Queue `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/queue/latest/actions/create-column-task" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "columnId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/queue/latest/actions/create-column-task', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "columnId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `columnId` | string | yes | Required path parameter from columns/:column_id/tasks. |
| `title` | string | no | Title of the task |
| `description` | string | no | Description of the task |
| `priority` | string | no | Priority level of the task |
| `deadline` | date | no | Deadline timestamp (ISO 8601) |
| `position` | number | no | Position of the task in its column |
| `coverUrl` | string | no | Optional cover image URL |

## Response

```json
{
  "success": true,
  "data": [
    {
      "coverUrl": "https://example.com",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "deadline": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "fields": {},
      "id": "string",
      "position": 1,
      "priority": "string",
      "sections": {},
      "title": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `coverUrl` | string | Optional cover image URL |
| `createdAt` | date | Timestamp when the task was created |
| `deadline` | date | Deadline timestamp for the task |
| `description` | string | Detailed description of the task |
| `fields` | object | Custom field values (key-value pairs) |
| `id` | string | Unique token ID of the task |
| `position` | number | Position within the column |
| `priority` | string | Priority level of the task |
| `sections` | object | Section-based field groupings (keyed by section ID) |
| `title` | string | Title of the task |
| `updatedAt` | date | Timestamp when the task was last updated |

## Native endpoint

Through the native Queue API, this operation is `POST columns/:column_id/tasks` (base URL `https://app.usequeue.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-column-task.md) for the provider-specific parameters and requirements.

