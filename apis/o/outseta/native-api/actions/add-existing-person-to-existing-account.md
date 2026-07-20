# Add Existing Person to Existing Account with Outseta

Adds an existing person to an existing account in Outseta.

## Endpoint

- **Method:** `POST`
- **Path:** `/crm/accounts/:accountUid/memberships`
- **Base URL:** `https://{subdomain}.outseta.com/api/v1`
- **Official documentation:** [Add Existing Person to Existing Account](https://documenter.getpostman.com/view/3613332/outseta-rest-api-v1/7TNfr6k)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `accountUid` | path | `string` | yes |
| `Person.Uid` | body | `string` | no |
| `IsPrimary` | body | `string` | no |
