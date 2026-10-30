# List Submissions with GoCanvas

## Endpoint

- **Method:** `GET`
- **Path:** `/submissions`
- **Base URL:** `https://www.gocanvas.com/api/v3`
- **Official documentation:** [List Submissions](https://api.gocanvas.com/api/v3/docs#list-all-submissions)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `form_id` | query | `number` | no | Filter by form; at least one of Form ID, User ID, or User Email is required. |
| `user_id` | query | `number` | no | Do not combine with User Email. |
| `user_email` | query | `string` | no | Do not combine with User ID. |
| `department_id` | query | `number` | no | Defaults to the user's default department. |
| `status` | query | `list` | no | Defaults to completed. Accepted values: `all`, `assigned`, `completed`, `custom`, `deleted`, `handed-off`, `in-progress`, `overdue`, `rejected`, `saved-to-cloud`, `unassigned`, `unfinished`. |
| `hand_off` | query | `string` | no | Required when Status is handed-off. |
| `custom_status` | query | `string` | no | Required when Status is custom. |
| `start_date` | query | `string` | no | Beginning of created-at range, in ISO 8601 format. |
| `end_date` | query | `string` | no | End of created-at range, in ISO 8601 format. |
