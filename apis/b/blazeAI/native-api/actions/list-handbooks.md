# List Handbooks with Blaze AI

Retrieves available handbooks from Blaze AI.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/w/:workspace_id/handbooks`
- **Base URL:** `https://api.blaze.ai`
- **Official documentation:** [List Handbooks](https://api.blaze.ai/api/documentation#!/handbooks/getApiV1WWorkspaceIdHandbooks)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `workspace_id` | path | `number` | yes |
