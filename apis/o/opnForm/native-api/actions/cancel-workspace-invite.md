# Cancel Workspace Invite with OpnForm

Cancels an invite in an OpnForm workspace.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/open/workspaces/:workspaceId/invites/:inviteId/cancel`
- **Base URL:** `https://api.opnform.com`
- **Official documentation:** [Cancel Workspace Invite](https://docs.opnform.com/api-reference/workspace-users/cancel-workspace-invite)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `workspaceId` | path | `number` | yes |
| `inviteId` | path | `number` | yes |
