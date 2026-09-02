# Update Project with Jetbuilt

## Endpoint

- **Method:** `PATCH`
- **Path:** `projects/:projectId`
- **Base URL:** `https://app.jetbuilt.com/api/`

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `custom_fields[].api_key` | body | `string` | no |
| `projectId` | path | `number` | yes |
| `custom_fields[].value` | body | `string` | no |
| `stage` | body | `string` | no |
| `custom_fields[]` | body | `array` | no |
| `client_id` | body | `string` | no |
| `paid_to_date` | body | `string` | no |
