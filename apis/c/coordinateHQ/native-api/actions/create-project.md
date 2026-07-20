# Create Project with CoordinateHQ

## Endpoint

- **Method:** `POST`
- **Path:** `/projects`
- **Base URL:** `https://app.coordinatehq.com/api/v1`
- **Official documentation:** [Create Project](https://app.coordinatehq.com/static/API_Documentation.html#projects)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `manager_email_address` | body | `string` | yes |
| `project_name` | body | `string` | yes |
| `external_object_id` | body | `string` | no |
| `playbook_name` | body | `string` | no |
| `stakeholder_email` | body | `string` | no |
| `stakeholder_task_assignment_list[]` | body | `array` | no |
