# Get full resolution screenshot URL with Worksnaps

Retrieves a full-resolution screenshot URL from Worksnaps.

## Endpoint

- **Method:** `GET`
- **Path:** `/projects/{project_id}/time_entries/{time_entry_id}.xml?full_resolution_url=1`
- **Base URL:** `https://api.worksnaps.com/api`
- **Official documentation:** [Get full resolution screenshot URL](https://api.worksnaps.com/api_docs/worksnaps.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | no | ID of the target project |
| `time_entry_id` | path | `string` | no | ID of the target Time Entry |
