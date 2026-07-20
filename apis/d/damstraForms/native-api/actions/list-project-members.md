# List Project Members with Damstra Forms

Retrieves project members from Damstra Forms.

## Endpoint

- **Method:** `GET`
- **Path:** `/projects/{project_id}/project_members`
- **Base URL:** `{baseUrl}`
- **Official documentation:** [List Project Members](https://sammapi.docs.apiary.io/#reference/project-members/project-member-collection/get-a-list-of-project-members)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | yes | The unique id (numeric) or uuid (string) of the project. |
