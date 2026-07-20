# Add Doc Access with Blaze AI

Creates a document access in Blaze AI.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/w/:workspace_id/docs/:doc_id/accesses`
- **Base URL:** `https://api.blaze.ai`
- **Official documentation:** [Add Doc Access](https://api.blaze.ai/api/documentation#!/accesses/postApiV1WWorkspaceIdDocsDocIdAccesses)

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
| `access[permission]` | body | `string` | yes | Access permission. |
| `access[accessor_type]` | body | `string` | yes | Accessor type. |
| `access[accessor_id]` | body | `number` | yes | Accessor record ID. |
