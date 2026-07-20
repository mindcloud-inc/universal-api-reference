# Submit Approval Request with Clockify

Submits an approval request in Clockify.

## Endpoint

- **Method:** `POST`
- **Path:** `workspaces/:workspaceId/approval-requests`
- **Base URL:** `https://api.clockify.me/api/v1`
- **Official documentation:** [Submit Approval Request](https://docs.developer.clockify.me/#tag/Approval/operation/createApprrovalRequest)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workspaceId` | path | `list<string>` | yes | — |
| `periodStart` | body | `string` | yes | — |
| `period` | body | `list<string>` | no | Accepted values: `MONTHLY`, `SEMI_MONTHLY`, `WEEKLY`. |
