# List Doc Accesses with Blaze AI

Retrieves document accesses from Blaze AI.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/w/:workspace_id/docs/:doc_id/accesses`
- **Base URL:** `https://api.blaze.ai`
- **Official documentation:** [List Doc Accesses](https://api.blaze.ai/api/documentation#!/accesses/getApiV1WWorkspaceIdDocsDocIdAccesses)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workspace_id` | path | `number` | yes | Blaze workspace ID. |
| `doc_id` | path | `number` | yes | Blaze document ID. |
