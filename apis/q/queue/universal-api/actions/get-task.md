# Queue: Get Task

Retrieves a task from Queue.

```
GET https://connect.mindcloud.co/v1/universal/queue/latest/actions/get-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Queue `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/queue/latest/actions/get-task?connectionId=$CONNECTION_ID&taskId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "taskId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/queue/latest/actions/get-task?${params}`, {
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
| `taskId` | string | yes |  |

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

Through the native Queue API, this operation is `GET tasks/:task_id` (base URL `https://app.usequeue.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-task.md) for the provider-specific parameters and requirements.

