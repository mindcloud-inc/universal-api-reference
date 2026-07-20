# Worksnaps: Get time entries in a project (for one or more users)

Retrieves time entries from a Worksnaps project.

```
GET https://connect.mindcloud.co/v1/universal/worksnaps/latest/actions/get-time-entries-in-a-project-for-one-or-more-users
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Worksnaps `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/worksnaps/latest/actions/get-time-entries-in-a-project-for-one-or-more-users?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/worksnaps/latest/actions/get-time-entries-in-a-project-for-one-or-more-users?${params}`, {
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
| `from_timestamp` | string | no | The starting timestamp. <br/>It must be at the boundary of a 10-minute interval. For example, 1300616400 (10:20am March 20, 2011 GMT) is valid while 1300616700 (10:25am March 20, 2011 GMT) is invalid. |
| `project_id` | string | no | ID of the target project |
| `task_ids` | string | no | &lt;task_ids&gt; can contain a sequence of IDs separated by semi-colon. |
| `time_entry_type` | string | no | specify whether to fetch online time or offline time entries. When not specified, both online and offline time entries will be fetched. |
| `to_timestamp` | string | no | The ending timnestamp. <br/>It must be at the boundary of a 10-minute interval |
| `user_ids` | string | no | &lt;user_ids&gt; can contain a sequence of IDs separated by semi-colon. |

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

Through the native Worksnaps API, this operation is `GET /projects/{project_id}/time_entries.xml` (base URL `https://api.worksnaps.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-time-entries-in-a-project-for-one-or-more-users.md) for the provider-specific parameters and requirements.

