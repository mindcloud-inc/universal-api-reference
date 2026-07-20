# Toggl Track: Delete Time Entry

Deletes an existing time entry from Toggl Track.

```
DELETE https://connect.mindcloud.co/v1/universal/togglTrack/latest/actions/delete-time-entry
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Toggl Track `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/togglTrack/latest/actions/delete-time-entry?connectionId=$CONNECTION_ID&workspaceId=1&timeEntryId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "workspaceId": "1",
  "timeEntryId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/togglTrack/latest/actions/delete-time-entry?${params}`, {
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
| `timeEntryId` | number | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "value": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `value` | string | The raw response body. The saved successful response was an empty string (HTTP 200). |

## Native endpoint

Through the native Toggl Track API, this operation is `DELETE /api/v9/workspaces/:workspace_id/time_entries/:time_entry_id` (base URL `https://api.track.toggl.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-time-entry.md) for the provider-specific parameters and requirements.

