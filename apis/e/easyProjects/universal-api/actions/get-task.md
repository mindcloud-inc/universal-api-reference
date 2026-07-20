# Easy Projects: Get Task

Retrieves a task from Easy Projects by ID.

```
GET https://connect.mindcloud.co/v1/universal/easyProjects/latest/actions/get-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Easy Projects `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/easyProjects/latest/actions/get-task?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/easyProjects/latest/actions/get-task?${params}`, {
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
| `id` | string | yes | Birdview task ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attachmentsCount": 1,
      "id": 1,
      "messagesCount": 1,
      "name": "Ava Chen",
      "priorityId": 1,
      "projectId": 1,
      "projectName": "Ava Chen",
      "statusId": 1,
      "taskTypeId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attachmentsCount` | number |  |
| `id` | number |  |
| `messagesCount` | number |  |
| `name` | string |  |
| `priorityId` | number |  |
| `projectId` | number |  |
| `projectName` | string |  |
| `statusId` | number |  |
| `taskTypeId` | number |  |

## Native endpoint

Through the native Easy Projects API, this operation is `GET /api/v1/tasks/:id` (base URL `https://api.go.easyprojects.net/api/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-task.md) for the provider-specific parameters and requirements.

