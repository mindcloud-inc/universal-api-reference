# Queue: Get Column Tasks

Retrieves tasks for a Queue column.

```
GET https://connect.mindcloud.co/v1/universal/queue/latest/actions/get-column-tasks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Queue `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/queue/latest/actions/get-column-tasks?connectionId=$CONNECTION_ID&columnId=string&projectId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "columnId": "string",
  "projectId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/queue/latest/actions/get-column-tasks?${params}`, {
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
| `columnId` | string | yes | Required path parameter from columns/:column_id/tasks. |
| `projectId` | string | yes |  |

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

Through the native Queue API, this operation is `GET columns/:column_id/tasks` (base URL `https://app.usequeue.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-column-tasks.md) for the provider-specific parameters and requirements.

