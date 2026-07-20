# 5pm: Create Task

Creates a new task in 5pm.

```
POST https://connect.mindcloud.co/v1/universal/pm/latest/actions/create-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a 5pm `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/pm/latest/actions/create-task" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "task.name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pm/latest/actions/create-task', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "task.name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `task.name` | string | yes | Name of the task to create. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "description": {},
        "endDate": {},
        "estimatedTime": "string",
        "flag": "string",
        "groupId": "string",
        "hidden": "string",
        "hoursDone": "string",
        "id": "string",
        "notifyClient": "string",
        "notifyProjectTeam": "string",
        "notifyTaskTeam": "string",
        "ownerId": 1,
        "parentId": "string",
        "prev": "string",
        "priority": 1,
        "progress": 1,
        "projectId": 1,
        "status": 1,
        "tags": {},
        "team": {
          "count": "string",
          "items": {},
          "total": "string"
        }
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data.description` | object |  |
| `data.endDate` | object |  |
| `data.estimatedTime` | string |  |
| `data.flag` | string |  |
| `data.groupId` | string |  |
| `data.hidden` | string |  |
| `data.hoursDone` | string |  |
| `data.id` | string |  |
| `data.notifyClient` | string |  |
| `data.notifyProjectTeam` | string |  |
| `data.notifyTaskTeam` | string |  |
| `data.ownerId` | number |  |
| `data.parentId` | string |  |
| `data.prev` | string |  |
| `data.priority` | number |  |
| `data.progress` | number |  |
| `data.projectId` | number |  |
| `data.status` | number |  |
| `data.tags` | object |  |
| `data.team.count` | string |  |
| `data.team.items` | object |  |
| `data.team.total` | string |  |

## Native endpoint

Through the native 5pm API, this operation is `POST /service/post/tasks/add` (base URL `{{credentials.workspaceUrl}}/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-task.md) for the provider-specific parameters and requirements.

