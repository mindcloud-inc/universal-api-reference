# Cancel Account with Outseta

Cancels an existing account in Outseta.

## Endpoint

- **Method:** `PUT`
- **Path:** `/crm/accounts/cancellation/:accountUid`
- **Base URL:** `https://{subdomain}.outseta.com/api/v1`
- **Official documentation:** [Cancel Account](https://documenter.getpostman.com/view/3613332/outseta-rest-api-v1/7TNfr6k)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `accountUid` | path | `string` | yes |
| `CancelationReason` | body | `string` | no |
| `Comment` | body | `string` | no |
