# Jostle: Update Task



```
PUT https://connect.mindcloud.co/v1/universal/jostle/latest/actions/update-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Jostle `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/jostle/latest/actions/update-task" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/jostle/latest/actions/update-task', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | Id of the task |
| `patches[0].op` | string | no | JSON Patch operation: add, remove, or replace |
| `patches[0].path` | string | no | JSON Pointer path to modify, for example /title |
| `patches[0].value` | string | no | Value used by the patch operation when required |

## Response

```json
{
  "success": true,
  "data": [
    {
      "assignee": {
        "username": "Ava Chen"
      },
      "collaborators": {
        "users": [
          {
            "username": "Ava Chen"
          }
        ]
      },
      "commentCount": 1,
      "completedTime": {},
      "completionStatus": true,
      "description": {},
      "dueDate": {},
      "taskState": "string",
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `assignee.username` | string |  |
| `collaborators.users[].username` | string |  |
| `commentCount` | number |  |
| `completedTime` | object |  |
| `completionStatus` | boolean |  |
| `description` | object |  |
| `dueDate` | object |  |
| `taskState` | string |  |
| `title` | string |  |

## Native endpoint

Through the native Jostle API, this operation is `PATCH /v2/tasks/task/:id` (base URL `https://api-prod.jostle.us`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-task.md) for the provider-specific parameters and requirements.

