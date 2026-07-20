# Get a time entry with Worksnaps

Retrieves a time entry from a Worksnaps project.

## Endpoint

- **Method:** `GET`
- **Path:** `/projects/{project_id}/time_entries/{time_entry_id}.xml`
- **Base URL:** `https://api.worksnaps.com/api`
- **Official documentation:** [Get a time entry](https://api.worksnaps.com/api_docs/worksnaps.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | no | ID of the target project |
| `time_entry_id` | path | `string` | no | ID of the Time Entry that needs to be fetched |
