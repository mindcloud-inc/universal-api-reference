# List Recent Templates for Workspace with Mural

Finds recent templates in Mural for a workspace.

## Endpoint

- **Method:** `GET`
- **Path:** `/workspaces/:workspaceId/templates/recent`
- **Base URL:** `https://app.mural.co/api/public/v1`
- **Official documentation:** [List Recent Templates for Workspace](https://developers.mural.co/public/reference/getrecenttemplates)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `withoutDefault` | query | `boolean` | no | Exclude default templates when true. |
| `workspaceId` | path | `string` | yes | Unique identifier of a workspace. |
