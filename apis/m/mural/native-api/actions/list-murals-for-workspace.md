# List Murals for Workspace with Mural

Finds murals in Mural for a workspace.

## Endpoint

- **Method:** `GET`
- **Path:** `/workspaces/:workspaceId/murals`
- **Base URL:** `https://app.mural.co/api/public/v1`
- **Official documentation:** [List Murals for Workspace](https://developers.mural.co/public/reference/getworkspacemurals)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `sortBy` | query | `string` | no | Sort murals by the documented Mural sort order. |
| `status` | query | `string` | no | Filter murals by active or archived status. |
| `workspaceId` | path | `string` | yes | Unique identifier of a workspace. |
