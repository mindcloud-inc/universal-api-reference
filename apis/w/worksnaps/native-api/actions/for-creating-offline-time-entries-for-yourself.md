# For creating offline time entries for YOURSELF with Worksnaps

Creates offline time entries for yourself in Worksnaps.

## Endpoint

- **Method:** `POST`
- **Path:** `/projects/{project_id}/time_entries.xml`
- **Base URL:** `https://api.worksnaps.com/api`
- **Official documentation:** [For creating offline time entries for YOURSELF](https://api.worksnaps.com/api_docs/worksnaps.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `body` | body | `string` | no | Raw XML request body for this Worksnaps endpoint. |
| `project_id` | path | `string` | no | ID of the target project |
