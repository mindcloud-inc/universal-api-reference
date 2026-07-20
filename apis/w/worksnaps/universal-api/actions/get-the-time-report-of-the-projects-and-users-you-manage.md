# Worksnaps: Get the time report of the projects and users you manage

Retrieves managed project time reports from Worksnaps.

```
GET https://connect.mindcloud.co/v1/universal/worksnaps/latest/actions/get-the-time-report-of-the-projects-and-users-you-manage
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Worksnaps `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/worksnaps/latest/actions/get-the-time-report-of-the-projects-and-users-you-manage?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/worksnaps/latest/actions/get-the-time-report-of-the-projects-and-users-you-manage?${params}`, {
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
| `from_date` | string | no | The starting date, in the format of YYYY-mm-dd. |
| `name` | string | no | this is a constant |
| `project_ids` | string | no | List of project IDs, separated by semi-colon. (If not specified, all of your managed projects will be used.) |
| `timezone_offset` | string | no | The timezone offset that is used to determine the timestamp associated with from_date and to_date. For example, 8, -8, +5.5, 0.<br>If not specified, the current user's timezone is used. |
| `to_date` | string | no | The ending date, in the format of YYYY-mm-dd. <br><br>The difference between from_date and to_date cannot be larger than 30 days. |
| `user_ids` | string | no | List of user IDs separated by semi-colon. (If not specified, all the users in your managed projects will be used.) |

## Response

```json
{
  "success": true,
  "data": [
    {
      "duration_in_minutes": 1,
      "project_id": 1,
      "task_id": "string",
      "task_name": "Ava Chen",
      "time_entry_type": "string",
      "user_comment": "string",
      "user_id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `duration_in_minutes` | number | the duration of the time entry (now it is always 10 minutes) |
| `project_id` | number | the ID of the project in which the time entry is logged |
| `task_id` | string | the ID of the task to which the entry is logged |
| `task_name` | string | the URL of the recorded webcam image |
| `time_entry_type` | string | the type of the time entry (online or offline) |
| `user_comment` | string | the comment that user entered when logging the time entry |
| `user_id` | string | the ID of the user who logged the time |

## Native endpoint

Through the native Worksnaps API, this operation is `GET /summary_reports` (base URL `https://api.worksnaps.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-the-time-report-of-the-projects-and-users-you-manage.md) for the provider-specific parameters and requirements.

