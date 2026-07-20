# List Project Lists with Damstra Forms

Retrieves project lists from Damstra Forms.

## Endpoint

- **Method:** `GET`
- **Path:** `/projects/{project_id}/project_lists`
- **Base URL:** `{baseUrl}`
- **Official documentation:** [List Project Lists](https://sammapi.docs.apiary.io/#reference/project-lists/project-list-collection/get-a-list-of-project-lists)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | yes | The unique id (numeric) or uuid (string) identifier of the project. |
