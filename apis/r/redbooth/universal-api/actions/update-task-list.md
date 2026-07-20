# Redbooth: Update Task List

Updates an existing task list in Redbooth.

```
PUT https://connect.mindcloud.co/v1/universal/redbooth/latest/actions/update-task-list
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Redbooth `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/redbooth/latest/actions/update-task-list" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1,
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/redbooth/latest/actions/update-task-list', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": 1,
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | number | yes | Redbooth task list ID |
| `name` | string | yes | Updated task list name |

## Response

```json
{
  "success": true,
  "data": [
    {
      "archived": true,
      "archived_tasks_count": 1,
      "deleted": true,
      "id": 1,
      "name": "Ava Chen",
      "project_id": 1,
      "tasks_count": 1,
      "type": "string",
      "user_id": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `archived` | boolean |  |
| `archived_tasks_count` | number |  |
| `deleted` | boolean |  |
| `id` | number |  |
| `name` | string |  |
| `project_id` | number |  |
| `tasks_count` | number |  |
| `type` | string |  |
| `user_id` | number |  |

## Native endpoint

Through the native Redbooth API, this operation is `PUT /task_lists/:id` (base URL `https://redbooth.com/api/3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-task-list.md) for the provider-specific parameters and requirements.

