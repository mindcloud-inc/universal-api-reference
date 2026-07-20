# Get time entries for a user in a project with Worksnaps

Retrieves a user's time entries from a Worksnaps project.

## Endpoint

- **Method:** `GET`
- **Path:** `/projects/{project_id}/users/{user_id}/time_entries.xml`
- **Base URL:** `https://api.worksnaps.com/api`
- **Official documentation:** [Get time entries for a user in a project](https://api.worksnaps.com/api_docs/worksnaps.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `from_timestamp` | query | `string` | no | The starting timestamp. <br/>It must be at the boundary of a 10-minute interval. For example, 1300616400 (10:20am March 20, 2011 GMT) is valid while 1300616700 (10:25am March 20, 2011 GMT) is invalid. |
| `project_id` | path | `string` | no | ID of the target project |
| `time_entry_type` | query | `string` | no | It specifies whether to fetch online time or offline time entries. When not specified, both online and offline time entries will be fetched. |
| `to_timestamp` | query | `string` | no | The ending timestamp. <br/>It must be at the boundary of a 10-minute interval |
| `user_id` | path | `string` | no | ID of the target user |
