# Todoist: Get Task

Retrieves task details from Todoist.

```
GET https://connect.mindcloud.co/v1/universal/todoist/latest/actions/get-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Todoist `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/todoist/latest/actions/get-task?connectionId=$CONNECTION_ID&taskId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "taskId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/todoist/latest/actions/get-task?${params}`, {
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
      "addedAt": "2026-05-07T12:00:00.000Z",
      "checked": true,
      "content": "string",
      "description": "string",
      "due": {},
      "id": "string",
      "isDeleted": true,
      "labels": [
        "string"
      ],
      "parentId": "string",
      "priority": 1,
      "projectId": "string",
      "sectionId": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `addedAt` | date |  |
| `checked` | boolean |  |
| `content` | string |  |
| `description` | string |  |
| `due` | object |  |
| `id` | string |  |
| `isDeleted` | boolean |  |
| `labels` | array<string> |  |
| `parentId` | string |  |
| `priority` | number |  |
| `projectId` | string |  |
| `sectionId` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Todoist API, this operation is `GET /api/v1/tasks/:task_id` (base URL `https://api.todoist.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-task.md) for the provider-specific parameters and requirements.

