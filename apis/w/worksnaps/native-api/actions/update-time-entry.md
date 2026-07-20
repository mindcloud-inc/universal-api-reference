# Update time entry with Worksnaps

Updates an existing time entry in Worksnaps.

## Endpoint

- **Method:** `PUT`
- **Path:** `/projects/{project_id}/time_entries/{time_entry_id}.xml`
- **Base URL:** `https://api.worksnaps.com/api`
- **Official documentation:** [Update time entry](https://api.worksnaps.com/api_docs/worksnaps.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `body` | body | `string` | no | Raw XML request body for this Worksnaps endpoint. |
| `project_id` | path | `string` | no | ID of the target project |
| `time_entry_id` | path | `string` | no | IDs of the target Time Entry to be updated, separated by semi-colon |
