# Add Workspace Member with DocuPanda - Document Understanding

Creates a workspace member in DocuPanda.

## Endpoint

- **Method:** `POST`
- **Path:** `/internal/workspace/member/add`
- **Base URL:** `https://app.docupipe.ai`
- **Official documentation:** [Add Workspace Member](https://docs.docupipe.ai/openapi/docupipe.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `invitedByEmail` | body | `string` | no | Email of the inviter |
| `memberEmail` | body | `string` | yes | Email of the member to add |
| `memberName` | body | `string` | no | Name of the member |
| `memberUserId` | body | `string` | yes | User ID of the member |
| `role` | body | `string` | no | Role to assign to the member |
| `workspaceId` | body | `string` | yes | ID of the workspace |
