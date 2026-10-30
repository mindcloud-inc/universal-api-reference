# List Dispatches with GoCanvas

## Endpoint

- **Method:** `GET`
- **Path:** `/dispatches`
- **Base URL:** `https://www.gocanvas.com/api/v3`
- **Official documentation:** [List Dispatches](https://api.gocanvas.com/api/v3/docs#list-all-dispatches)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `user_id` | query | `number` | no | Assigned user ID. Provide at least one of User ID, Department ID, or Form ID. |
| `department_id` | query | `number` | no | Department ID. Provide at least one of User ID, Department ID, or Form ID. |
| `form_id` | query | `number` | no | Form ID. Provide at least one of User ID, Department ID, or Form ID. |
| `project_id` | query | `number` | no | Restrict results to dispatches assigned to this project. |
| `status` | query | `list` | no | Ready ignores date filters and returns eligible assigned or received dispatches for the requested/current user. Accepted values: `assigned`, `ready`, `received`, `unassigned`. |
| `start_date` | query | `string` | no | Beginning bound for created_at, in ISO 8601. |
| `end_date` | query | `string` | no | Ending bound for created_at, in ISO 8601. |
| `scheduled_start_date` | query | `string` | no | Beginning bound for scheduled_at, in ISO 8601. |
| `scheduled_end_date` | query | `string` | no | Ending bound for scheduled_end, in ISO 8601. |
