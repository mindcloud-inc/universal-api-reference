# Resubmit Entries and Expenses for Approval with Clockify

Resubmits entries and expenses for approval in Clockify.

## Endpoint

- **Method:** `POST`
- **Path:** `workspaces/:workspaceId/approval-requests/resubmit-entries-for-approval`
- **Base URL:** `https://api.clockify.me/api/v1`
- **Official documentation:** [Resubmit Entries and Expenses for Approval](https://docs.developer.clockify.me/#tag/Approval/operation/resubmitApprovalRequest)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workspaceId` | path | `list<string>` | yes | — |
| `periodStart` | body | `string` | yes | — |
| `period` | body | `list<string>` | no | Accepted values: `MONTHLY`, `SEMI_MONTHLY`, `WEEKLY`. |
