# Toggl Track: Update Task

Updates an existing task in Toggl Track.

```
PUT https://connect.mindcloud.co/v1/universal/togglTrack/latest/actions/update-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Toggl Track `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/togglTrack/latest/actions/update-task" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "workspaceId": 1,
  "projectId": 1,
  "taskId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/togglTrack/latest/actions/update-task', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "workspaceId": 1,
    "projectId": 1,
    "taskId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `workspaceId` | list<number> | yes |  |
| `projectId` | list<number> | yes |  |
| `taskId` | list<number> | yes |  |
| `name` | string | no |  |
| `active` | boolean | no |  |
| `estimatedSeconds` | number | no |  |
| `userId` | number | no |  |
| `externalReference` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "active": true,
      "at": "string",
      "estimatedSeconds": {},
      "id": 1,
      "name": "Ava Chen",
      "projectId": 1,
      "recurring": true,
      "serverDeletedAt": {},
      "trackedSeconds": 1,
      "userId": {},
      "workspaceId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean |  |
| `at` | string |  |
| `estimatedSeconds` | object |  |
| `id` | number |  |
| `name` | string |  |
| `projectId` | number |  |
| `recurring` | boolean |  |
| `serverDeletedAt` | object |  |
| `trackedSeconds` | number |  |
| `userId` | object |  |
| `workspaceId` | number |  |

## Native endpoint

Through the native Toggl Track API, this operation is `PUT /api/v9/workspaces/:workspace_id/projects/:project_id/tasks/:task_id` (base URL `https://api.track.toggl.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-task.md) for the provider-specific parameters and requirements.

