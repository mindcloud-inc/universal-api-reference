# Update Deal with Outseta

Updates an existing deal in Outseta.

## Endpoint

- **Method:** `PUT`
- **Path:** `/crm/deals/:dealUid`
- **Base URL:** `https://{subdomain}.outseta.com/api/v1`
- **Official documentation:** [Update Deal](https://documenter.getpostman.com/view/3613332/outseta-rest-api-v1/7TNfr6k)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `dealUid` | path | `string` | yes |
| `Name` | body | `string` | no |
| `DealPipelineStage.Uid` | body | `string` | no |
| `Amount` | body | `number` | no |
| `AssignedToPersonClientIdentifier` | body | `string` | no |
| `Account.Uid` | body | `string` | no |
| `DealPeople[].Person.Uid` | body | `string` | no |
