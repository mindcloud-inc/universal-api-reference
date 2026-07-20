# Remove Doc Access with Blaze AI

Deletes an existing document access from Blaze AI.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/api/v1/w/:workspace_id/docs/:doc_id/accesses/:id`
- **Base URL:** `https://api.blaze.ai`
- **Official documentation:** [Remove Doc Access](https://api.blaze.ai/api/documentation#!/accesses/deleteApiV1WWorkspaceIdDocsDocIdAccessesId)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workspace_id` | path | `number` | yes | Blaze workspace ID. |
| `doc_id` | path | `number` | yes | Blaze document ID. |
| `id` | path | `number` | yes | Blaze access record ID. |
