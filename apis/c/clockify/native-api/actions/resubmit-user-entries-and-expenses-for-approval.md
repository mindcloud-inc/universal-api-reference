# Resubmit User Entries and Expenses for Approval with Clockify

Resubmits a user's entries and expenses for approval in Clockify.

## Endpoint

- **Method:** `POST`
- **Path:** `workspaces/:workspaceId/approval-requests/users/:userId/resubmit-entries-for-approval`
- **Base URL:** `https://api.clockify.me/api/v1`
- **Official documentation:** [Resubmit User Entries and Expenses for Approval](https://docs.developer.clockify.me/#tag/Approval/operation/resubmitApprovalRequestForOther)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workspaceId` | path | `list<string>` | yes | — |
| `userId` | path | `string<string>` | yes | — |
| `periodStart` | body | `string` | yes | — |
| `period` | body | `list<string>` | no | Accepted values: `MONTHLY`, `SEMI_MONTHLY`, `WEEKLY`. |
