# List Approval Requests with Clockify

Lists all approval requests in Clockify.

## Endpoint

- **Method:** `GET`
- **Path:** `workspaces/:workspaceId/approval-requests`
- **Base URL:** `https://api.clockify.me/api/v1`
- **Official documentation:** [List Approval Requests](https://docs.developer.clockify.me/#tag/Approval/operation/getApprovalRequests)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workspaceId` | path | `list<string>` | yes | Workspace identifier |
| `status` | query | `list<string>` | no | Accepted values: `APPROVED`, `PENDING`, `WITHDRAWN_APPROVAL`. |
