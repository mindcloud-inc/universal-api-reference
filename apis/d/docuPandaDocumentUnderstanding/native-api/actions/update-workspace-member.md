# Update Workspace Member with DocuPanda - Document Understanding

Updates an existing workspace member in DocuPanda.

## Endpoint

- **Method:** `POST`
- **Path:** `/internal/workspace/member/update`
- **Base URL:** `https://app.docupipe.ai`
- **Official documentation:** [Update Workspace Member](https://docs.docupipe.ai/openapi/docupipe.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `action` | body | `string` | yes | Action to perform: 'update_role' or 'remove' |
| `memberUserId` | body | `string` | yes | User ID of the member to update |
| `newRole` | body | `string` | no | New role for the member (if action is update_role) |
| `workspaceId` | body | `string` | yes | ID of the workspace |
