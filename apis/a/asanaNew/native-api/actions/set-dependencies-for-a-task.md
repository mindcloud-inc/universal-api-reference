# Set dependencies for a task with Asana

Sets dependencies for a task in Asana.

## Endpoint

- **Method:** `POST`
- **Path:** `tasks/:task_gid/addDependencies`
- **Base URL:** `https://app.asana.com/api/1.0`
- **Official documentation:** [Set dependencies for a task](https://developers.asana.com/reference/adddependenciesfortask)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `data.dependencies[]` | body | `array<string>` | yes |
| `task_gid` | path | `string` | yes |
