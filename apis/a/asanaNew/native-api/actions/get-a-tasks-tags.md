# Get a task's tags with Asana

Retrieves a task's tags from Asana.

## Endpoint

- **Method:** `GET`
- **Path:** `tasks/:task_gid/tags`
- **Base URL:** `https://app.asana.com/api/1.0`
- **Official documentation:** [Get a task's tags](https://developers.asana.com/reference/gettagsfortask)

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
