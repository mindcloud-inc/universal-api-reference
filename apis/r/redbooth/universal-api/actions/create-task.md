# Redbooth: Create Task

Creates a new task in Redbooth.

```
POST https://connect.mindcloud.co/v1/universal/redbooth/latest/actions/create-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Redbooth `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/redbooth/latest/actions/create-task" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "taskListId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/redbooth/latest/actions/create-task', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "taskListId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | Task name |
| `taskListId` | number | yes | Target Redbooth task list ID |
| `description` | string | no | Task description |

## Response

```json
{
  "success": true,
  "data": [
    {
      "comments_count": 1,
      "description": "string",
      "id": 1,
      "name": "Ava Chen",
      "project_id": 1,
      "status": "string",
      "task_list_id": 1,
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `comments_count` | number |  |
| `description` | string |  |
| `id` | number |  |
| `name` | string |  |
| `project_id` | number |  |
| `status` | string |  |
| `task_list_id` | number |  |
| `type` | string |  |

## Native endpoint

Through the native Redbooth API, this operation is `POST /tasks` (base URL `https://redbooth.com/api/3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-task.md) for the provider-specific parameters and requirements.

