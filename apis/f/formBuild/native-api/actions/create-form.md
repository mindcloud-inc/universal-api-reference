# Create Form with 123FormBuild

Creates a new form in 123FormBuilder.

## Endpoint

- **Method:** `POST`
- **Path:** `/forms`
- **Base URL:** `https://api.123formbuilder.com/v2`
- **Official documentation:** [Create Form](https://www.123formbuilder.com/developer/api-v2-forms/)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | The name of the new form |
| `group_id` | body | `number` | no | The ID of the group in which you want to create the form |
| `active` | body | `number` | no | Form activity status |
| `active_date_from` | body | `date` | no | Start date when active status is period-based |
| `active_date_to` | body | `date` | no | End date when active status is period-based |
| `active_days` | body | `string` | no | Comma-separated day numbers when active status is weekly |
