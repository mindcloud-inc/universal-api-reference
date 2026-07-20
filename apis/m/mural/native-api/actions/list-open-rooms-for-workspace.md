# List Open Rooms for Workspace with Mural

Finds open rooms in Mural for a workspace.

## Endpoint

- **Method:** `GET`
- **Path:** `/workspaces/:workspaceId/rooms/open`
- **Base URL:** `https://app.mural.co/api/public/v1`
- **Official documentation:** [List Open Rooms for Workspace](https://developers.mural.co/public/reference/getworkspaceopenrooms)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workspaceId` | path | `string` | yes | Unique identifier of a workspace. |
