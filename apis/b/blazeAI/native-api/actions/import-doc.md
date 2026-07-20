# Import Doc with Blaze AI

Creates a document import in Blaze AI.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/w/:workspace_id/imports`
- **Base URL:** `https://api.blaze.ai`
- **Official documentation:** [Import Doc](https://api.blaze.ai/api/documentation#!/imports/postApiV1WWorkspaceIdImports)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `workspace_id` | path | `number` | yes |
| `import[file]` | body | `string` | yes |
| `import[source]` | body | `string` | yes |
