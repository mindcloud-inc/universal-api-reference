# Update Form with 123FormBuild

Updates an existing form in 123FormBuilder.

## Endpoint

- **Method:** `PUT`
- **Path:** `/forms/{form_id}`
- **Base URL:** `https://api.123formbuilder.com/v2`
- **Official documentation:** [Update Form](https://www.123formbuilder.com/developer/api-v2-forms/)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `form_id` | path | `number` | yes | The ID of the form |
| `name` | body | `string` | no | Change the name of the form |
| `group_id` | body | `number` | no | The ID of the group in which you want to place the form |
| `active` | body | `number` | no | Form activity status |
| `active_date_from` | body | `date` | no | Start date when active status is period-based |
| `active_date_to` | body | `date` | no | End date when active status is period-based |
| `active_days` | body | `string` | no | Comma-separated day numbers when active status is weekly |
