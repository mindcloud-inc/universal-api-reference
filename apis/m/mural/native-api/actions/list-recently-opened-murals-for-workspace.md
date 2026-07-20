# List Recently Opened Murals for Workspace with Mural

Finds recently opened murals in Mural for a workspace.

## Endpoint

- **Method:** `GET`
- **Path:** `/workspaces/:workspaceId/murals/recent`
- **Base URL:** `https://app.mural.co/api/public/v1`
- **Official documentation:** [List Recently Opened Murals for Workspace](https://developers.mural.co/public/reference/getworkspacerecentmurals)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workspaceId` | path | `string` | yes | Unique identifier of a workspace. |
