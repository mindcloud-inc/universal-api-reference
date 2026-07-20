# Redbooth: Create Task List

Creates a new task list in Redbooth.

```
POST https://connect.mindcloud.co/v1/universal/redbooth/latest/actions/create-task-list
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Redbooth `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/redbooth/latest/actions/create-task-list" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "projectId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/redbooth/latest/actions/create-task-list', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "projectId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | Task list name |
| `projectId` | number | yes | Parent project ID |

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

Through the native Redbooth API, this operation is `POST /task_lists` (base URL `https://redbooth.com/api/3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-task-list.md) for the provider-specific parameters and requirements.

