# Create a user assignment (i.e., assign a user to a project) with Worksnaps

Creates a user assignment in a Worksnaps project.

## Endpoint

- **Method:** `POST`
- **Path:** `/projects/{project_id}/user_assignments.xml`
- **Base URL:** `https://api.worksnaps.com/api`
- **Official documentation:** [Create a user assignment (i.e., assign a user to a project)](https://api.worksnaps.com/api_docs/worksnaps.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `body` | body | `string` | no | Raw XML request body for this Worksnaps endpoint. |
| `project_id` | path | `string` | no | ID of the target project |
