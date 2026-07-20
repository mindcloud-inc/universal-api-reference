# Change Policy Status with Clockify

Updates a policy status in Clockify.

## Endpoint

- **Method:** `PATCH`
- **Path:** `workspaces/:workspaceId/time-off/policies/:id`
- **Base URL:** `https://api.clockify.me/api/v1`
- **Official documentation:** [Change Policy Status](https://docs.developer.clockify.me/#tag/Policy/operation/updatePolicyStatus)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workspaceId` | path | `list<string>` | yes | — |
| `id` | path | `string<string>` | yes | — |
| `status` | body | `list<string>` | yes | Accepted values: `ACTIVE`, `ALL`, `ARCHIVED`. |
