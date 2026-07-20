# List Doc Properties with Blaze AI

Retrieves document properties from Blaze AI.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/w/:workspace_id/docs/:doc_id/properties`
- **Base URL:** `https://api.blaze.ai`
- **Official documentation:** [List Doc Properties](https://api.blaze.ai/api/documentation#!/properties/getApiV1WWorkspaceIdDocsDocIdProperties)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workspace_id` | path | `number` | yes | Blaze workspace ID. |
| `doc_id` | path | `number` | yes | Blaze document ID. |
