# Copy a Schema to Another Workspace with DocuPanda - Document Understanding

Creates a schema copy in another DocuPanda workspace.

## Endpoint

- **Method:** `POST`
- **Path:** `/copy/schema`
- **Base URL:** `https://app.docupipe.ai`
- **Official documentation:** [Copy a Schema to Another Workspace](https://docs.docupipe.ai/reference/post_copy_schema)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `schemaId` | body | `string` | yes | Unique identifier of the schema to copy. |
| `targetWorkspaceApiKey` | body | `string` | yes | API key of the target workspace to copy the schema to. |
