# List Handbook Items with Blaze AI

Retrieves handbook items from Blaze AI.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/w/:workspace_id/handbooks/:handbook_id/items`
- **Base URL:** `https://api.blaze.ai`
- **Official documentation:** [List Handbook Items](https://api.blaze.ai/api/documentation#!/handbook%20items/getApiV1WWorkspaceIdHandbooksHandbookIdItems)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `workspace_id` | path | `number` | yes |
| `handbook_id` | path | `number` | yes |
