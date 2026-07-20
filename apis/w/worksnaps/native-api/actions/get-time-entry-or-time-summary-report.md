# Get time entry or time summary report with Worksnaps

Retrieves a project time report from Worksnaps.

## Endpoint

- **Method:** `GET`
- **Path:** `/projects/{project_id}/reports`
- **Base URL:** `https://api.worksnaps.com/api`
- **Official documentation:** [Get time entry or time summary report](https://api.worksnaps.com/api_docs/worksnaps.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `from_timestamp` | query | `string` | no | The starting timestamp. <br/>It must be at the boundary of a 10-minute interval. For example, 1300616400 (10:20am March 20, 2011 GMT) is valid while 1300616700 (10:25am March 20, 2011 GMT) is invalid. |
| `name` | query | `string` | no | The type of report, either time entries ('time_entries') and time summary ('time_summary') |
| `project_id` | path | `string` | no | ID of the target project for which the reported is generated |
| `task_ids` | query | `string` | no | List of task IDs separated by semi-colon. |
| `time_entry_type` | query | `string` | no | whether to include only online or offline time. <br/>If not specified, the report will include both online and offline time. |
| `to_timestamp` | query | `string` | no | The ending timestamp. <br/>It must be at the boundary of a 10-minute interval. <br><br>The difference between from_timestamp and to_timestamp cannot be larger than 30 days. |
| `user_ids` | query | `string` | no | List of user IDs separated by semi-colon. (Note: when querying time entries (i.e., name=time_entries) this field is required.) |
