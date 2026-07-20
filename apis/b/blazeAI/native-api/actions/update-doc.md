# Update Doc with Blaze AI

Updates an existing document in Blaze AI.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/api/v1/w/:workspace_id/docs/:id`
- **Base URL:** `https://api.blaze.ai`
- **Official documentation:** [Update Doc](https://api.blaze.ai/api/documentation#!/docs/patchApiV1WWorkspaceIdDocsId)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/x-www-form-urlencoded` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workspace_id` | path | `number` | yes | Blaze workspace ID. |
| `id` | path | `number` | yes | Blaze document ID. |
| `doc[title]` | body | `string` | yes | Updated Blaze document title. |
