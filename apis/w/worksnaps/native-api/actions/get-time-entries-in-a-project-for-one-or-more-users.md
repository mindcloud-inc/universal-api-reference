# Get time entries in a project (for one or more users) with Worksnaps

Retrieves time entries from a Worksnaps project.

## Endpoint

- **Method:** `GET`
- **Path:** `/projects/{project_id}/time_entries.xml`
- **Base URL:** `https://api.worksnaps.com/api`
- **Official documentation:** [Get time entries in a project (for one or more users)](https://api.worksnaps.com/api_docs/worksnaps.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `from_timestamp` | query | `string` | no | The starting timestamp. <br/>It must be at the boundary of a 10-minute interval. For example, 1300616400 (10:20am March 20, 2011 GMT) is valid while 1300616700 (10:25am March 20, 2011 GMT) is invalid. |
| `project_id` | path | `string` | no | ID of the target project |
| `task_ids` | query | `string` | no | &lt;task_ids&gt; can contain a sequence of IDs separated by semi-colon. |
| `time_entry_type` | query | `string` | no | specify whether to fetch online time or offline time entries. When not specified, both online and offline time entries will be fetched. |
| `to_timestamp` | query | `string` | no | The ending timnestamp. <br/>It must be at the boundary of a 10-minute interval |
| `user_ids` | query | `string` | no | &lt;user_ids&gt; can contain a sequence of IDs separated by semi-colon. |
