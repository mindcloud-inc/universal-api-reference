# Update Person Account Membership with Outseta

Updates an existing account membership in Outseta.

## Endpoint

- **Method:** `PUT`
- **Path:** `/crm/accounts/:accountUid/memberships/:membershipUid`
- **Base URL:** `https://{subdomain}.outseta.com/api/v1`
- **Official documentation:** [Update Person Account Membership](https://documenter.getpostman.com/view/3613332/outseta-rest-api-v1/7TNfr6k)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `accountUid` | path | `string` | yes |
| `membershipUid` | path | `string` | yes |
| `Person.Uid` | body | `string` | no |
| `IsPrimary` | body | `string` | no |
