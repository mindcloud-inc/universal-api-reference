# List Groups with Blaze AI

Retrieves workspace groups from Blaze AI.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/w/:workspace_id/groups`
- **Base URL:** `https://api.blaze.ai`
- **Official documentation:** [List Groups](https://api.blaze.ai/api/documentation#!/groups/getApiV1WWorkspaceIdGroups)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `workspace_id` | path | `number` | yes |
