# ProjectManager: Create Or Update TaskAssignee

Creates or updates task assignees in ProjectManager.

```
PUT https://connect.mindcloud.co/v1/universal/projectManager/latest/actions/create-or-update-task-assignee
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ProjectManager `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/projectManager/latest/actions/create-or-update-task-assignee" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "taskId": "22222222-2222-2222-2222-222222222222",
  "value[]": "sample"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/projectManager/latest/actions/create-or-update-task-assignee', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "taskId": "22222222-2222-2222-2222-222222222222",
    "value[]": "sample",
    "value[]": "sample",
    "value[]": "sample",
    "value[]": "sample"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `taskId` | string | yes | The unique identifier of the Task to add or update an assignment Example: `22222222-2222-2222-2222-222222222222`. |
| `value[]` | array | yes | Example: `sample`. |
| `value[]` | array | yes | Example: `sample`. |
| `value[]` | array | yes | Example: `sample`. |
| `value[]` | array | yes | Example: `sample`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "changeSetId": "string",
      "id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `changeSetId` | string |  |
| `id` | string |  |

## Native endpoint

Through the native ProjectManager API, this operation is `PUT /api/data/tasks/:taskId/assignees` (base URL `https://api.projectmanager.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-or-update-task-assignee.md) for the provider-specific parameters and requirements.

