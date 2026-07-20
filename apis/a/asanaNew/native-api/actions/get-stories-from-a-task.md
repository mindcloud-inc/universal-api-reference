# Get stories from a task with Asana

Retrieves stories for a task from Asana.

## Endpoint

- **Method:** `GET`
- **Path:** `tasks/:task_gid/stories`
- **Base URL:** `https://app.asana.com/api/1.0`
- **Official documentation:** [Get stories from a task](https://developers.asana.com/reference/getstoriesfortask)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `limit` | query | `number` | no | — |
| `offset` | query | `string` | no | — |
| `opt_fields[]` | query | `array<string>` | no | This endpoint returns a compact resource, excluding most properties by default. To include additional properties in the response add them here. |
| `task_gid` | path | `string` | yes | — |
