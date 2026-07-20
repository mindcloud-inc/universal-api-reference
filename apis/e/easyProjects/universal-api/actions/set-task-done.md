# Easy Projects: Set Task Done

Marks an Easy Projects task as done.

```
PUT https://connect.mindcloud.co/v1/universal/easyProjects/latest/actions/set-task-done
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Easy Projects `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/easyProjects/latest/actions/set-task-done" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "123"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/easyProjects/latest/actions/set-task-done', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "123"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | Birdview task ID. Example: `123`. |

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

Through the native Easy Projects API, this operation is `PUT /api/v1/tasks/:id/done` (base URL `https://api.go.easyprojects.net/api/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/set-task-done.md) for the provider-specific parameters and requirements.

