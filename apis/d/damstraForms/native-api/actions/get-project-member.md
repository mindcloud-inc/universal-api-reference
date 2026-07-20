# Get Project Member with Damstra Forms

Retrieves a project member from Damstra Forms.

## Endpoint

- **Method:** `GET`
- **Path:** `/projects/{project_id}/project_members/{user_id}`
- **Base URL:** `{baseUrl}`
- **Official documentation:** [Get Project Member](https://sammapi.docs.apiary.io/#reference/project-members/project-member-instance/get-a-project-member)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | yes | The unique id (numeric) or uuid (string) of the project. |
| `user_id` | path | `string` | yes | The unique id (numeric) or uuid (string) of the user. |
