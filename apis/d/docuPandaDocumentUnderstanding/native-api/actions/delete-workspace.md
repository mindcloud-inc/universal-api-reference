# Delete Workspace with DocuPanda - Document Understanding

Deletes an existing workspace from DocuPanda.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/internal/workspace/delete`
- **Base URL:** `https://app.docupipe.ai`
- **Official documentation:** [Delete Workspace](https://docs.docupipe.ai/openapi/docupipe.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workspaceId` | body | `string` | yes | ID of the workspace to delete |
