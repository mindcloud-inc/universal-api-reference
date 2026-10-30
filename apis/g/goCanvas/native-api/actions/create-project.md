# Create Project with GoCanvas

## Endpoint

- **Method:** `POST`
- **Path:** `/projects`
- **Base URL:** `https://www.gocanvas.com/api/v3`
- **Official documentation:** [Create Project](https://api.gocanvas.com/api/v3/docs#create-a-project)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | — |
| `department_id` | body | `number` | no | — |
| `customer_id` | body | `number` | no | — |
| `site_id` | body | `number` | no | — |
| `start_date` | body | `string` | no | ISO 8601 date or datetime. |
| `end_date` | body | `string` | no | ISO 8601 date or datetime. |
| `status` | body | `list` | no | One of: active, inactive, draft. Accepted values: `active`, `draft`, `inactive`. |
| `notes` | body | `string` | no | — |
| `code` | body | `string` | no | — |
