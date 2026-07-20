# Update Approval Request with Clockify

Updates an approval request in Clockify.

## Endpoint

- **Method:** `PATCH`
- **Path:** `workspaces/:workspaceId/approval-requests/:approvalRequestId`
- **Base URL:** `https://api.clockify.me/api/v1`
- **Official documentation:** [Update Approval Request](https://docs.developer.clockify.me/#tag/Approval/operation/updateApprovalStatus)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workspaceId` | path | `list<string>` | yes | — |
| `approvalRequestId` | path | `string<string>` | yes | — |
| `state` | body | `list<string>` | yes | Accepted values: `APPROVED`, `PENDING`, `REJECTED`, `WITHDRAWN_APPROVAL`, `WITHDRAWN_SUBMISSION`. |
| `note` | body | `string` | no | — |
