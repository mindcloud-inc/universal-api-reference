# Add Doc Property with Blaze AI

Creates a document property in Blaze AI.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/w/:workspace_id/docs/:doc_id/properties`
- **Base URL:** `https://api.blaze.ai`
- **Official documentation:** [Add Doc Property](https://api.blaze.ai/api/documentation#!/properties/postApiV1WWorkspaceIdDocsDocIdProperties)

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
| `property_id` | body | `number` | yes | Workspace property ID. |
| `value` | body | `string` | no | Property value. |
