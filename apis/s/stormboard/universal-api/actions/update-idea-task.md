# Stormboard: Update Idea Task

Updates an idea task in Stormboard.

```
PUT https://connect.mindcloud.co/v1/universal/stormboard/latest/actions/update-idea-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Stormboard `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/stormboard/latest/actions/update-idea-task" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "ideaId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/stormboard/latest/actions/update-idea-task', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "ideaId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `assignedTo` | string | no | Stormboard user ID to assign to the task. |
| `dateCompleted` | string | no | Task completion date in YYYY-MM-DD format. |
| `dateDue` | string | no | Task due date in YYYY-MM-DD format. |
| `ideaId` | number | yes | Idea ID from a Stormboard idea record. |
| `notify` | string | no | Set to 1 to notify the assignee, or 0 to skip the notification. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "status": 1,
      "task": {
        "action": "string",
        "assignees": [
          {}
        ],
        "date": {
          "assigned": "string",
          "due": "string"
        },
        "idea": {
          "id": 1
        },
        "status": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `status` | number |  |
| `task` | object |  |
| `task.action` | string |  |
| `task.assignees` | array<object> |  |
| `task.date` | object |  |
| `task.date.assigned` | string |  |
| `task.date.due` | string |  |
| `task.idea` | object |  |
| `task.idea.id` | number |  |
| `task.status` | string |  |

## Native endpoint

Through the native Stormboard API, this operation is `PUT /ideas/:idea_id/task` (base URL `https://api.stormboard.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-idea-task.md) for the provider-specific parameters and requirements.

