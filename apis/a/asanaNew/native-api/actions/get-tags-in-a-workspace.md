# Get tags in a workspace with Asana

Retrieves tags in an Asana workspace.

## Endpoint

- **Method:** `GET`
- **Path:** `workspaces/:workspace_gid/tags`
- **Base URL:** `https://app.asana.com/api/1.0`
- **Official documentation:** [Get tags in a workspace](https://developers.asana.com/reference/gettagsforworkspace)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workspace_gid` | path | `string` | yes | Asana workspace gid parameter. |
| `opt_pretty` | query | `boolean` | no | Asana opt pretty parameter. |
| `limit` | query | `number` | no | Asana limit parameter. |
| `offset` | query | `string` | no | Asana offset parameter. |
| `opt_fields` | query | `list<string>` | no | Asana opt fields parameter. |
