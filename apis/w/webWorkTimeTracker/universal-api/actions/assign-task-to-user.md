# WebWork Time Tracker: Assign Task to User

Assigns a task to a user in WebWork Time Tracker.

```
PUT https://connect.mindcloud.co/v1/universal/webWorkTimeTracker/latest/actions/assign-task-to-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WebWork Time Tracker `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/webWorkTimeTracker/latest/actions/assign-task-to-user" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "taskId": 1,
  "userId": 1,
  "workspaceId": 1,
  "projectId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/webWorkTimeTracker/latest/actions/assign-task-to-user', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "taskId": 1,
    "userId": 1,
    "workspaceId": 1,
    "projectId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `taskId` | number | yes | ID of the task. |
| `userId` | number | yes | ID of the user to assign the task to. |
| `workspaceId` | number | yes | Workspace ID. |
| `projectId` | number | yes | Project ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": 1,
      "taskId": "string",
      "userId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number |  |
| `taskId` | string |  |
| `userId` | string |  |

## Native endpoint

Through the native WebWork Time Tracker API, this operation is `POST /tasks/:taskId/assign/:userId` (base URL `https://api.webwork-tracker.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/assign-task-to-user.md) for the provider-specific parameters and requirements.

