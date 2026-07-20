# Add a tag to a task with Asana

Adds a tag to a task in Asana.

## Endpoint

- **Method:** `POST`
- **Path:** `tasks/:task_gid/addTag`
- **Base URL:** `https://app.asana.com/api/1.0`
- **Official documentation:** [Add a tag to a task](https://developers.asana.com/reference/addtagfortask)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `data.tag` | body | `string` | yes |
| `task_gid` | path | `string` | yes |
