# Submit User Approval Request with Clockify

Submits an approval request for a user in Clockify.

## Endpoint

- **Method:** `POST`
- **Path:** `workspaces/:workspaceId/approval-requests/users/:userId`
- **Base URL:** `https://api.clockify.me/api/v1`
- **Official documentation:** [Submit User Approval Request](https://docs.developer.clockify.me/#tag/Approval/operation/createApprovalForOther)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workspaceId` | path | `list<string>` | yes | — |
| `userId` | path | `string<string>` | yes | — |
| `periodStart` | body | `string` | yes | — |
| `period` | body | `list<string>` | no | Accepted values: `MONTHLY`, `SEMI_MONTHLY`, `WEEKLY`. |
