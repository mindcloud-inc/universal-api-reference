# Set Temporary Password with Outseta

Sets a temporary password for a person in Outseta.

## Endpoint

- **Method:** `PUT`
- **Path:** `/crm/people/:personUid/setTemporaryPassword`
- **Base URL:** `https://{subdomain}.outseta.com/api/v1`
- **Official documentation:** [Set Temporary Password](https://documenter.getpostman.com/view/3613332/outseta-rest-api-v1/7TNfr6k)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `personUid` | path | `string` | yes |
| `temporaryPassword` | body | `string` | no |
