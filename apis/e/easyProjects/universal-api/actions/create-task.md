# Easy Projects: Create Task

Creates a new task in Easy Projects.

```
POST https://connect.mindcloud.co/v1/universal/easyProjects/latest/actions/create-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Easy Projects `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/easyProjects/latest/actions/create-task" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "model": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/easyProjects/latest/actions/create-task', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "model": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `model` | object | yes | Task creation model. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attachmentsCount": 1,
      "description": "string",
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
| `description` | string |  |
| `id` | number |  |
| `messagesCount` | number |  |
| `name` | string |  |
| `priorityId` | number |  |
| `projectId` | number |  |
| `projectName` | string |  |
| `statusId` | number |  |
| `taskTypeId` | number |  |

## Native endpoint

Through the native Easy Projects API, this operation is `POST /api/v1/tasks` (base URL `https://api.go.easyprojects.net/api/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-task.md) for the provider-specific parameters and requirements.

