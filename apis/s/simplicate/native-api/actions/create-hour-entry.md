# Create Hour Entry with Simplicate

## Endpoint

- **Method:** `POST`
- **Path:** `/hours/hours`
- **Base URL:** `https://{subdomain}/api/v2`
- **Official documentation:** [Create Hour Entry](https://developer.simplicate.com/docs/api/v2/reference/create-hours-hours/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `employee_id` | body | `string` | no | Employee identifier. |
| `hours` | body | `string` | no | Number of hours. |
| `note` | body | `string` | no | Hour entry note. |
| `project_id` | body | `string` | no | Project identifier. |
| `projectservice_id` | body | `string` | no | Project service identifier. |
| `source` | body | `string` | no | Hours source. |
| `start_date` | body | `string` | no | Entry start date in YYYY-MM-DD format. |
| `type_id` | body | `string` | no | Hour type identifier. |
