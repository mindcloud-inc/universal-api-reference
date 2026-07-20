# Remove Workspace Member By Email with DocuPanda - Document Understanding

Deletes a workspace member by email from DocuPanda.

## Endpoint

- **Method:** `POST`
- **Path:** `/internal/workspace/member/remove-by-email`
- **Base URL:** `https://app.docupipe.ai`
- **Official documentation:** [Remove Workspace Member By Email](https://docs.docupipe.ai/openapi/docupipe.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `memberEmail` | body | `string` | yes | Email of the member to remove |
| `workspaceId` | body | `string` | yes | ID of the workspace |
