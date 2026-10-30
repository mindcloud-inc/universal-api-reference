# Update Project with GoCanvas

## Endpoint

- **Method:** `PATCH`
- **Path:** `/projects/:projectId`
- **Base URL:** `https://www.gocanvas.com/api/v3`
- **Official documentation:** [Update Project](https://api.gocanvas.com/api/v3/docs#update-a-project)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `number` | yes | Identifier of the project to update. |
| `name` | body | `string` | no | Project name; PATCH documentation conflicts on whether it is required. |
| `department_id` | body | `number` | no | Department associated with the project. |
| `customer_id` | body | `number` | no | Customer associated with the project; the documentation example sends null. |
| `site_id` | body | `number` | no | Site associated with the customer; the documentation example sends null. |
| `start_date` | body | `string` | no | Project start date or datetime in ISO 8601 format. |
| `end_date` | body | `string` | no | Project end date or datetime in ISO 8601 format. |
| `status` | body | `list` | no | Project status. Accepted values: `active`, `draft`, `inactive`. |
| `notes` | body | `string` | no | Longer description of the project. |
| `code` | body | `string` | no | Alphanumeric code uniquely identifying the project. |
