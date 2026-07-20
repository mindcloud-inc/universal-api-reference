# Update Hour Entry with Simplicate

## Endpoint

- **Method:** `PUT`
- **Path:** `/hours/hours/:id`
- **Base URL:** `https://{subdomain}/api/v2`
- **Official documentation:** [Update Hour Entry](https://developer.simplicate.com/docs/api/v2/reference/update-hours-hours/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `employee_id` | body | `string` | no | Employee identifier. |
| `hours` | body | `string` | no | Number of hours. |
| `id` | path | `string` | no | Hour entry identifier. |
| `note` | body | `string` | no | Hour entry note. |
| `project_id` | body | `string` | no | Project identifier. |
| `projectservice_id` | body | `string` | no | Project service identifier. |
| `source` | body | `string` | no | Hours source. |
| `start_date` | body | `string` | no | Entry start date in YYYY-MM-DD format. |
| `type_id` | body | `string` | no | Hour type identifier. |
