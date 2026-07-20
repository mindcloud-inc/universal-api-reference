# Toggl Track: List Time Entries

Retrieves time entries from Toggl Track.

```
GET https://connect.mindcloud.co/v1/universal/togglTrack/latest/actions/list-time-entries
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Toggl Track `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/togglTrack/latest/actions/list-time-entries?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/togglTrack/latest/actions/list-time-entries?${params}`, {
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
| `since` | number | no |  |
| `before` | number | no |  |
| `startDate` | date | no |  |
| `endDate` | date | no |  |
| `meta` | boolean | no |  |
| `includeSharing` | boolean | no |  |

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

Through the native Toggl Track API, this operation is `GET /api/v9/me/time_entries` (base URL `https://api.track.toggl.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-time-entries.md) for the provider-specific parameters and requirements.

