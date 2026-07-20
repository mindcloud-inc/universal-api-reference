# List Timesheets with Procore

Retrieves timesheets from Procore.

## Endpoint

- **Method:** `GET`
- **Path:** `/rest/v1.0/projects/:project_id/timesheets`
- **Base URL:** `https://api.procore.com`
- **Official documentation:** [List Timesheets](https://developers.procore.com/reference/rest/timesheets#list-all-timesheets)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | yes | Unique identifier for the project. |
