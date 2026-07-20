# Get Project List with Damstra Forms

Retrieves a project list from Damstra Forms.

## Endpoint

- **Method:** `GET`
- **Path:** `/projects/{project_id}/project_lists/{project_list_type_id}`
- **Base URL:** `{baseUrl}`
- **Official documentation:** [Get Project List](https://sammapi.docs.apiary.io/#reference/project-lists/project-list-instance/get-a-project-list)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | yes | The unique id (numeric) or uuid (string) identifier of the project. |
| `project_list_type_id` | path | `string` | yes | The unique id (numeric) or uuid (string) identifier of the project list type. |
