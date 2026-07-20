# Get Doc with Blaze AI

Retrieves a document from Blaze AI.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/w/:workspace_id/docs/:id`
- **Base URL:** `https://api.blaze.ai`
- **Official documentation:** [Get Doc](https://api.blaze.ai/api/documentation#!/docs/getApiV1WWorkspaceIdDocsId)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workspace_id` | path | `number` | yes | Blaze workspace ID. |
| `id` | path | `number` | yes | Blaze document ID. |
