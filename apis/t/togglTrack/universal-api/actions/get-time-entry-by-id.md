# Toggl Track: Get Time Entry By ID

Retrieves a time entry by ID from Toggl Track.

```
GET https://connect.mindcloud.co/v1/universal/togglTrack/latest/actions/get-time-entry-by-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Toggl Track `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/togglTrack/latest/actions/get-time-entry-by-id?connectionId=$CONNECTION_ID&timeEntryId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "timeEntryId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/togglTrack/latest/actions/get-time-entry-by-id?${params}`, {
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
| `timeEntryId` | number | yes |  |

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
      "userId": 1,
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
| `userId` | number |  |
| `workspaceId` | number |  |

## Native endpoint

Through the native Toggl Track API, this operation is `GET /api/v9/me/time_entries/:time_entry_id` (base URL `https://api.track.toggl.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-time-entry-by-id.md) for the provider-specific parameters and requirements.

