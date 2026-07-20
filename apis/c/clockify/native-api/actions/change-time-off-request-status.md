# Change Time Off Request Status with Clockify

Updates a time off request status in Clockify.

## Endpoint

- **Method:** `PATCH`
- **Path:** `workspaces/:workspaceId/time-off/policies/:policyId/requests/:requestId`
- **Base URL:** `https://api.clockify.me/api/v1`
- **Official documentation:** [Change Time Off Request Status](https://docs.developer.clockify.me/#tag/Time-Off/operation/changeTimeOffRequestStatus)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workspaceId` | path | `list<string>` | yes | — |
| `policyId` | path | `string<string>` | yes | — |
| `requestId` | path | `string<string>` | yes | — |
| `note` | body | `string` | no | — |
| `status` | body | `list<string>` | no | Accepted values: `APPROVED`, `REJECTED`. |
