# Get sections in a project with Asana

Retrieves sections in a project from Asana.

## Endpoint

- **Method:** `GET`
- **Path:** `projects/:project_gid/sections`
- **Base URL:** `https://app.asana.com/api/1.0`
- **Official documentation:** [Get sections in a project](https://developers.asana.com/reference/getsectionsforproject)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `limit` | query | `number` | no | — |
| `project_gid` | path | `string` | yes | Path parameter: project_gid |
| `offset` | query | `string` | no | — |
| `opt_fields[]` | query | `array<string>` | no | — |
