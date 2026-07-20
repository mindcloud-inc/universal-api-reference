# Asana: Create a subtask

Creates a subtask in Asana.

```
POST https://connect.mindcloud.co/v1/universal/asanaNew/latest/actions/create-a-subtask
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Asana `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/asanaNew/latest/actions/create-a-subtask" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "taskGid": "string",
  "data": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/asanaNew/latest/actions/create-a-subtask', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "taskGid": "string",
    "data": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `optFields[]` | array<string> | no |  |
| `taskGid` | string | yes | Path parameter: task_gid |
| `data` | object | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "actualTimeMinutes": 1,
      "assignee": {},
      "assigneeStatus": "string",
      "completed": true,
      "completedAt": "2026-05-07T12:00:00.000Z",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "dueAt": "2026-05-07T12:00:00.000Z",
      "dueOn": "2026-05-07T12:00:00.000Z",
      "followers": [
        {
          "gid": "string",
          "name": "Ava Chen",
          "resourceType": "string"
        }
      ],
      "gid": "string",
      "hearted": true,
      "liked": true,
      "modifiedAt": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "notes": "string",
      "numHearts": 1,
      "numLikes": 1,
      "parent": {
        "gid": "string",
        "name": "Ava Chen",
        "resourceSubtype": "string",
        "resourceType": "string"
      },
      "permalinkUrl": "https://example.com",
      "resourceSubtype": "string",
      "resourceType": "string",
      "startAt": "2026-05-07T12:00:00.000Z",
      "startOn": "2026-05-07T12:00:00.000Z",
      "workspace": {
        "gid": "string",
        "name": "Ava Chen",
        "resourceType": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `actualTimeMinutes` | number |  |
| `assignee` | object |  |
| `assigneeStatus` | string |  |
| `completed` | boolean |  |
| `completedAt` | date |  |
| `createdAt` | date |  |
| `dueAt` | date |  |
| `dueOn` | date |  |
| `followers[].gid` | string |  |
| `followers[].name` | string |  |
| `followers[].resourceType` | string |  |
| `gid` | string |  |
| `hearted` | boolean |  |
| `liked` | boolean |  |
| `modifiedAt` | date |  |
| `name` | string |  |
| `notes` | string |  |
| `numHearts` | number |  |
| `numLikes` | number |  |
| `parent.gid` | string |  |
| `parent.name` | string |  |
| `parent.resourceSubtype` | string |  |
| `parent.resourceType` | string |  |
| `permalinkUrl` | string |  |
| `resourceSubtype` | string |  |
| `resourceType` | string |  |
| `startAt` | date |  |
| `startOn` | date |  |
| `workspace.gid` | string |  |
| `workspace.name` | string |  |
| `workspace.resourceType` | string |  |

## Native endpoint

Through the native Asana API, this operation is `POST tasks/:task_gid/subtasks` (base URL `https://app.asana.com/api/1.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-a-subtask.md) for the provider-specific parameters and requirements.

