# List Rooms for Workspace with Mural

Finds rooms in Mural for a workspace.

## Endpoint

- **Method:** `GET`
- **Path:** `/workspaces/:workspaceId/rooms`
- **Base URL:** `https://app.mural.co/api/public/v1`
- **Official documentation:** [List Rooms for Workspace](https://developers.mural.co/public/reference/getworkspacerooms)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workspaceId` | path | `string` | yes | Unique identifier of a workspace. |
