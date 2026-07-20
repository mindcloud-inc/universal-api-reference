# Update a task with Asana

Updates a task in Asana.

## Endpoint

- **Method:** `PUT`
- **Path:** `tasks/:task_gid`
- **Base URL:** `https://app.asana.com/api/1.0`
- **Official documentation:** [Update a task](https://developers.asana.com/reference/updatetask)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `data.custom_field` | body | `object` | no | — |
| `data.custom_field.gid` | body | `string` | no | The GID of the custom field that you want to update the value of. |
| `opt_fields[]` | query | `array<string>` | no | — |
| `task_gid` | path | `string` | yes | — |
| `data` | body | `object` | yes | — |
| `data.custom_field.value` | body | `string` | no | Value can be a GID, string, number, etc... For date, use format "YYYY-MM-DD" (e.g., 2019-09-15). For date-time, use ISO 8601 date string in UTC (e.g., 2019-09-15T02:06:58.147Z). |
