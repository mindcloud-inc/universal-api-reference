# Update Workspace Name with DocuPanda - Document Understanding

Updates an existing workspace name in DocuPanda.

## Endpoint

- **Method:** `PUT`
- **Path:** `/internal/workspace/update-name`
- **Base URL:** `https://app.docupipe.ai`
- **Official documentation:** [Update Workspace Name](https://docs.docupipe.ai/openapi/docupipe.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | New name for the workspace |
| `workspaceId` | body | `string` | yes | ID of the workspace |
