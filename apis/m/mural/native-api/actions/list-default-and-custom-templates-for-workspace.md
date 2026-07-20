# List Default and Custom Templates for Workspace with Mural

Finds default and custom templates in Mural for a workspace.

## Endpoint

- **Method:** `GET`
- **Path:** `/workspaces/:workspaceId/templates`
- **Base URL:** `https://app.mural.co/api/public/v1`
- **Official documentation:** [List Default and Custom Templates for Workspace](https://developers.mural.co/public/reference/gettemplatesbyworkspace)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `withoutDefault` | query | `boolean` | no | Exclude default templates when true. |
| `workspaceId` | path | `string` | yes | Unique identifier of a workspace. |
