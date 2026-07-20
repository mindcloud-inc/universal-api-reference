# Delete a user assignment with Worksnaps

Deletes an existing user assignment from Worksnaps.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/projects/{project_id}/user_assignments/{user_assignment_id}.xml`
- **Base URL:** `https://api.worksnaps.com/api`
- **Official documentation:** [Delete a user assignment](https://api.worksnaps.com/api_docs/worksnaps.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | no | ID of the target project |
| `user_assignment_id` | path | `string` | no | ID of the user assignment to be deleted |
