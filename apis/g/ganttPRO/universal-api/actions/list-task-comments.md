# GanttPRO: List Task Comments

Retrieves comments for a specific GanttPRO task.

```
GET https://connect.mindcloud.co/v1/universal/ganttPRO/latest/actions/list-task-comments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GanttPRO `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ganttPRO/latest/actions/list-task-comments?connectionId=$CONNECTION_ID&taskId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "taskId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ganttPRO/latest/actions/list-task-comments?${params}`, {
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
| `taskId` | number | yes | Required task identifier. GanttPRO accepts this as an array-style query parameter. Accepts multiple values as an array. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "comment": "string",
      "content": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "is_removed": 1,
      "projectId": 1,
      "taskId": 1,
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "user": {},
      "userId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `comment` | string |  |
| `content` | string |  |
| `createdAt` | date |  |
| `id` | number |  |
| `is_removed` | number |  |
| `projectId` | number |  |
| `taskId` | number |  |
| `updatedAt` | date |  |
| `user` | object |  |
| `userId` | number |  |

## Native endpoint

Through the native GanttPRO API, this operation is `GET /comments` (base URL `https://api.ganttpro.com/v1.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-task-comments.md) for the provider-specific parameters and requirements.

