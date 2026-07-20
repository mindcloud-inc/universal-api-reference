# Update a user assignment with Worksnaps

Updates an existing user assignment in Worksnaps.

## Endpoint

- **Method:** `PUT`
- **Path:** `/projects/{project_id}/user_assignments/{user_assignment_id}.xml`
- **Base URL:** `https://api.worksnaps.com/api`
- **Official documentation:** [Update a user assignment](https://api.worksnaps.com/api_docs/worksnaps.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `body` | body | `string` | no | Raw XML request body for this Worksnaps endpoint. |
| `project_id` | path | `string` | no | ID of the target project |
| `user_assignment_id` | path | `string` | no | ID of the user assignment to be updated |
