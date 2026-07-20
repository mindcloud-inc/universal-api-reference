# Toggl Track: Get Task

Retrieves a task from Toggl Track.

```
GET https://connect.mindcloud.co/v1/universal/togglTrack/latest/actions/get-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Toggl Track `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/togglTrack/latest/actions/get-task?connectionId=$CONNECTION_ID&workspaceId=1&projectId=1&taskId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "workspaceId": "1",
  "projectId": "1",
  "taskId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/togglTrack/latest/actions/get-task?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `workspaceId` | number | yes |  |
| `projectId` | number | yes |  |
| `taskId` | number | yes |  |

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

Through the native Toggl Track API, this operation is `GET /api/v9/workspaces/:workspace_id/projects/:project_id/tasks/:task_id` (base URL `https://api.track.toggl.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-task.md) for the provider-specific parameters and requirements.

