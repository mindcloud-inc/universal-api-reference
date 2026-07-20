# Toggl Track: Stop Time Entry

Stops an existing time entry in Toggl Track.

```
PUT https://connect.mindcloud.co/v1/universal/togglTrack/latest/actions/stop-time-entry
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Toggl Track `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/togglTrack/latest/actions/stop-time-entry" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "workspaceId": 1,
  "timeEntryId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/togglTrack/latest/actions/stop-time-entry', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "workspaceId": 1,
    "timeEntryId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `workspaceId` | list<number> | yes |  |
| `timeEntryId` | list<number> | yes |  |

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
      "stop": "string",
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
| `stop` | string |  |
| `taskId` | object |  |
| `uid` | number |  |
| `userId` | number |  |
| `wid` | number |  |
| `workspaceId` | number |  |

## Native endpoint

Through the native Toggl Track API, this operation is `PATCH /api/v9/workspaces/:workspace_id/time_entries/:time_entry_id/stop` (base URL `https://api.track.toggl.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/stop-time-entry.md) for the provider-specific parameters and requirements.

