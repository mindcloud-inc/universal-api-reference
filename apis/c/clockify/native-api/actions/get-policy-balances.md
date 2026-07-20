# Get Policy Balances with Clockify

Retrieves time off policy balances from Clockify.

## Endpoint

- **Method:** `GET`
- **Path:** `workspaces/:workspaceId/time-off/balance/policy/:policyId`
- **Base URL:** `https://api.clockify.me/api/v1`
- **Official documentation:** [Get Policy Balances](https://docs.developer.clockify.me/#tag/Balance/operation/getBalancesForPolicy)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `workspaceId` | path | `list<string>` | yes |
| `policyId` | path | `string<string>` | yes |
