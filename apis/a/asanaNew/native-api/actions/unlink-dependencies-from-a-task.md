# Unlink dependencies from a task with Asana

Removes dependencies from a task in Asana.

## Endpoint

- **Method:** `POST`
- **Path:** `tasks/:task_gid/removeDependencies`
- **Base URL:** `https://app.asana.com/api/1.0`
- **Official documentation:** [Unlink dependencies from a task](https://developers.asana.com/reference/removedependenciesfortask)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `data.dependencies[]` | body | `array<string>` | yes |
| `opt_pretty` | query | `string` | no |
| `task_gid` | path | `string` | yes |
