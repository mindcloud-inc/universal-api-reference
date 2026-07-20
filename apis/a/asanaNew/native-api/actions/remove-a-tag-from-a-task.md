# Remove a tag from a task with Asana

Removes a tag from a task in Asana.

## Endpoint

- **Method:** `POST`
- **Path:** `tasks/:task_gid/removeTag`
- **Base URL:** `https://app.asana.com/api/1.0`
- **Official documentation:** [Remove a tag from a task](https://developers.asana.com/reference/removetagfortask)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `data.tag` | body | `string` | yes |
| `task_gid` | path | `string` | yes |
| `opt_pretty` | query | `boolean` | no |
