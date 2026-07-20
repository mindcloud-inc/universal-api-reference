# Delete time entry with Worksnaps

Deletes an existing time entry from Worksnaps.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/projects/{project_id}/time_entries/{time_entry_id}.xml`
- **Base URL:** `https://api.worksnaps.com/api`
- **Official documentation:** [Delete time entry](https://api.worksnaps.com/api_docs/worksnaps.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | no | ID of the target project |
| `time_entry_id` | path | `string` | no | IDs of the target Time Entry that needs to be deleted, separated by semi-colon. |
