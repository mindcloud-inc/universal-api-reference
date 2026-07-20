# Get dependencies from a task with Asana

Retrieves dependencies for a task from Asana.

## Endpoint

- **Method:** `GET`
- **Path:** `tasks/:task_gid/dependencies`
- **Base URL:** `https://app.asana.com/api/1.0`
- **Official documentation:** [Get dependencies from a task](https://developers.asana.com/reference/getdependenciesfortask)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `task_gid` | path | `string` | yes |
| `opt_pretty` | query | `boolean` | no |
| `opt_fields` | query | `list<string>` | no |
