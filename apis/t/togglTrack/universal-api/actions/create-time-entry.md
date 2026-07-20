# Toggl Track: Create Time Entry

Creates a new time entry in Toggl Track.

```
POST https://connect.mindcloud.co/v1/universal/togglTrack/latest/actions/create-time-entry
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Toggl Track `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/togglTrack/latest/actions/create-time-entry" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "workspaceId": 1,
  "wid": 1,
  "createdWith": "string",
  "start": "2026-05-07T12:00:00.000Z"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/togglTrack/latest/actions/create-time-entry', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "workspaceId": 1,
    "wid": 1,
    "createdWith": "string",
    "start": "2026-05-07T12:00:00.000Z"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `workspaceId` | number | yes |  |
| `wid` | number | yes |  |
| `createdWith` | string | yes |  |
| `start` | date | yes |  |
| `duration` | number | no |  |
| `description` | string | no |  |
| `projectId` | number | no |  |
| `taskId` | number | no |  |
| `billable` | boolean | no |  |
| `meta` | boolean | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "at": "string",
      "billable": true,
      "description": "string",
      "duration": 1,
      "duronly": true,
      "id": 1,
      "projectId": {},
      "serverDeletedAt": {},
      "start": "string",
      "stop": {},
      "tagIds": {},
      "tags": {},
      "taskId": {},
      "uid": 1,
      "userId": 1,
      "wid": 1,
      "workspaceId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `at` | string |  |
| `billable` | boolean |  |
| `description` | string |  |
| `duration` | number |  |
| `duronly` | boolean |  |
| `id` | number |  |
| `projectId` | object |  |
| `serverDeletedAt` | object |  |
| `start` | string |  |
| `stop` | object |  |
| `tagIds` | object |  |
| `tags` | object |  |
| `taskId` | object |  |
| `uid` | number |  |
| `userId` | number |  |
| `wid` | number |  |
| `workspaceId` | number |  |

## Native endpoint

Through the native Toggl Track API, this operation is `POST /api/v9/workspaces/:workspace_id/time_entries` (base URL `https://api.track.toggl.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-time-entry.md) for the provider-specific parameters and requirements.

