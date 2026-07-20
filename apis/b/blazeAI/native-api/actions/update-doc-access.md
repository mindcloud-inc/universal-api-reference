# Update Doc Access with Blaze AI

Updates an existing document access in Blaze AI.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/api/v1/w/:workspace_id/docs/:doc_id/accesses/:id`
- **Base URL:** `https://api.blaze.ai`
- **Official documentation:** [Update Doc Access](https://api.blaze.ai/api/documentation#!/accesses/patchApiV1WWorkspaceIdDocsDocIdAccessesId)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/x-www-form-urlencoded` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workspace_id` | path | `number` | yes | Blaze workspace ID. |
| `doc_id` | path | `number` | yes | Blaze document ID. |
| `id` | path | `number` | yes | Blaze access record ID. |
| `access[permission]` | body | `string` | yes | Updated access permission. |
