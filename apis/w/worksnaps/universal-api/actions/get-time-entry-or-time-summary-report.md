# Worksnaps: Get time entry or time summary report

Retrieves a project time report from Worksnaps.

```
GET https://connect.mindcloud.co/v1/universal/worksnaps/latest/actions/get-time-entry-or-time-summary-report
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Worksnaps `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/worksnaps/latest/actions/get-time-entry-or-time-summary-report?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/worksnaps/latest/actions/get-time-entry-or-time-summary-report?${params}`, {
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
| `name` | string | no | The type of report, either time entries ('time_entries') and time summary ('time_summary') |
| `project_id` | string | no | ID of the target project for which the reported is generated |
| `task_ids` | string | no | List of task IDs separated by semi-colon. |
| `time_entry_type` | string | no | whether to include only online or offline time. <br/>If not specified, the report will include both online and offline time. |
| `to_timestamp` | string | no | The ending timestamp. <br/>It must be at the boundary of a 10-minute interval. <br><br>The difference between from_timestamp and to_timestamp cannot be larger than 30 days. |
| `user_ids` | string | no | List of user IDs separated by semi-colon. (Note: when querying time entries (i.e., name=time_entries) this field is required.) |

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

Through the native Worksnaps API, this operation is `GET /projects/{project_id}/reports` (base URL `https://api.worksnaps.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-time-entry-or-time-summary-report.md) for the provider-specific parameters and requirements.

