# Delete Time Off Request with Clockify

Deletes a time off request from Clockify.

## Endpoint

- **Method:** `DELETE`
- **Path:** `workspaces/:workspaceId/time-off/policies/:policyId/requests/:requestId`
- **Base URL:** `https://api.clockify.me/api/v1`
- **Official documentation:** [Delete Time Off Request](https://docs.developer.clockify.me/#tag/Time-Off/operation/deleteTimeOffRequest)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `workspaceId` | path | `list<string>` | yes |
| `policyId` | path | `string<string>` | yes |
| `requestId` | path | `string<string>` | yes |
