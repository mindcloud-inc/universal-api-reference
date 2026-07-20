# Remove Workspace Member with DocuPanda - Document Understanding

Deletes a workspace member from DocuPanda.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/internal/workspace/member/remove`
- **Base URL:** `https://app.docupipe.ai`
- **Official documentation:** [Remove Workspace Member](https://docs.docupipe.ai/openapi/docupipe.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `memberEmail` | body | `string` | no | Email of the member to remove |
| `memberUserId` | body | `string` | no | User ID of the member to remove |
| `workspaceId` | body | `string` | yes | ID of the workspace |
