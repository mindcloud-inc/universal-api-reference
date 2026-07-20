# Leave Workspace with DocuPanda - Document Understanding

Deletes your workspace membership from DocuPanda.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/internal/workspace/leave`
- **Base URL:** `https://app.docupipe.ai`
- **Official documentation:** [Leave Workspace](https://docs.docupipe.ai/openapi/docupipe.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workspaceId` | body | `string` | yes | ID of the workspace to leave |
