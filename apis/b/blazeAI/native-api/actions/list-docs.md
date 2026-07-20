# List Docs with Blaze AI

Retrieves documents from a Blaze AI workspace.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/w/:workspace_id/docs`
- **Base URL:** `https://api.blaze.ai`
- **Official documentation:** [List Docs](https://api.blaze.ai/api/documentation#!/docs/getApiV1WWorkspaceIdDocs)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workspace_id` | path | `number` | yes | Blaze workspace ID. |
| `folder_id` | query | `number` | no | Optional folder filter. |
