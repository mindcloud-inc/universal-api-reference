# Remove followers from a task with Asana

Removes followers from a task in Asana.

## Endpoint

- **Method:** `POST`
- **Path:** `tasks/:task_gid/removeFollowers`
- **Base URL:** `https://app.asana.com/api/1.0`
- **Official documentation:** [Remove followers from a task](https://developers.asana.com/reference/removefollowerfortask)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `data.followers[]` | body | `array<string>` | yes |
| `task_gid` | path | `string` | yes |
