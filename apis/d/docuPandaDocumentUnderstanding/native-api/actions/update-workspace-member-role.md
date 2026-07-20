# Update Workspace Member Role with DocuPanda - Document Understanding

Updates a workspace member role in DocuPanda.

## Endpoint

- **Method:** `POST`
- **Path:** `/internal/workspace/member/update-role`
- **Base URL:** `https://app.docupipe.ai`
- **Official documentation:** [Update Workspace Member Role](https://docs.docupipe.ai/openapi/docupipe.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `memberEmail` | body | `string` | yes | Email of the member to update |
| `role` | body | `string` | yes | New role for the member |
| `workspaceId` | body | `string` | yes | ID of the workspace |
