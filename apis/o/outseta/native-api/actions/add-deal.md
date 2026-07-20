# Add Deal with Outseta

Creates a new deal in Outseta.

## Endpoint

- **Method:** `POST`
- **Path:** `/crm/deals`
- **Base URL:** `https://{subdomain}.outseta.com/api/v1`
- **Official documentation:** [Add Deal](https://documenter.getpostman.com/view/3613332/outseta-rest-api-v1/7TNfr6k)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `Name` | body | `string` | no |
| `DealPipelineStage.Uid` | body | `string` | no |
| `Amount` | body | `number` | no |
| `AssignedToPersonClientIdentifier` | body | `string` | no |
| `Account.Uid` | body | `string` | no |
| `DealPeople[].Person.Uid` | body | `string` | no |
