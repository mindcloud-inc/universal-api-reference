# Get dependents from a task with Asana

Retrieves dependents for a task from Asana.

## Endpoint

- **Method:** `GET`
- **Path:** `tasks/:task_gid/dependents`
- **Base URL:** `https://app.asana.com/api/1.0`
- **Official documentation:** [Get dependents from a task](https://developers.asana.com/reference/getdependentsfortask)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `task_gid` | path | `string` | yes | Asana task gid parameter. |
| `opt_pretty` | query | `boolean` | no | Asana opt pretty parameter. |
| `limit` | query | `number` | no | Asana limit parameter. |
| `offset` | query | `string` | no | Asana offset parameter. |
| `opt_fields` | query | `list<string>` | no | Asana opt fields parameter. |
