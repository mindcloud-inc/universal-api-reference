# Worksnaps: Get a time entry

Retrieves a time entry from a Worksnaps project.

```
GET https://connect.mindcloud.co/v1/universal/worksnaps/latest/actions/get-a-time-entry
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Worksnaps `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/worksnaps/latest/actions/get-a-time-entry?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/worksnaps/latest/actions/get-a-time-entry?${params}`, {
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
| `project_id` | string | no | ID of the target project |
| `time_entry_id` | string | no | ID of the Time Entry that needs to be fetched |

## Response

```json
{
  "success": true,
  "data": [
    {
      "activities": "string",
      "activity_level": 1,
      "duration_in_minutes": 1,
      "from_timestamp": "string",
      "id": 1,
      "logged_timestamp": "string",
      "project_id": 1,
      "task_id": "string",
      "thumbnail_url": "https://example.com",
      "type": "string",
      "user_comment": "string",
      "user_id": "string",
      "webcam_url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `activities` | string |  |
| `activity_level` | number | the activity level (0 to 10) of the time entry |
| `duration_in_minutes` | number | the duration of the time entry (now it is always 10 minutes) |
| `from_timestamp` | string | the starting timestamp of the time entry (each time entry represents 10 minutes) |
| `id` | number | the ID of the time entry |
| `logged_timestamp` | string | the timestamp that the time entry is logged |
| `project_id` | number | the ID of the project in which the time entry is logged |
| `task_id` | string | the ID of the task to which the entry is logged |
| `thumbnail_url` | string | the URL of the recorded thumbnail screen shot image |
| `type` | string | the type of the time entry (either online or offline) |
| `user_comment` | string | the comment that user entered when logging the time entry |
| `user_id` | string | the ID of the user who logged the time |
| `webcam_url` | string | the URL of the recorded webcam image |

## Native endpoint

Through the native Worksnaps API, this operation is `GET /projects/{project_id}/time_entries/{time_entry_id}.xml` (base URL `https://api.worksnaps.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-a-time-entry.md) for the provider-specific parameters and requirements.

