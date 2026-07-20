# Remove Person from Account with Outseta

Removes a person from an account in Outseta.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/crm/accounts/:accountUid/memberships/:membershipUid`
- **Base URL:** `https://{subdomain}.outseta.com/api/v1`
- **Official documentation:** [Remove Person from Account](https://documenter.getpostman.com/view/3613332/outseta-rest-api-v1/7TNfr6k)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `accountUid` | path | `string` | yes |
| `membershipUid` | path | `string` | yes |
