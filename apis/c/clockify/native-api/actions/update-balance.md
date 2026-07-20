# Update Balance with Clockify

Updates a time off balance in Clockify.

## Endpoint

- **Method:** `PATCH`
- **Path:** `workspaces/:workspaceId/time-off/balance/policy/:policyId`
- **Base URL:** `https://api.clockify.me/api/v1`
- **Official documentation:** [Update Balance](https://docs.developer.clockify.me/#tag/Balance/operation/updateBalance)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `workspaceId` | path | `list<string>` | yes |
| `policyId` | path | `string<string>` | yes |
| `userIds[]` | body | `array<string>` | yes |
| `value` | body | `number` | yes |
| `note` | body | `string` | no |
