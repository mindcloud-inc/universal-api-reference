# Update Role with Meisterplan

Updates an existing role in Meisterplan.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/roles/:roleId`
- **Base URL:** `https://api.us.meisterplan.com/v1`
- **Official documentation:** [Update Role](https://api.us.meisterplan.com/docs/api.html#operation/UpdateRole)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `roleId` | path | `string` | yes |
| `name` | body | `string` | no |
| `externalId` | body | `string` | no |
| `costType` | body | `string` | no |
| `obsUnits` | body | `object` | no |
| `resourceManager` | body | `object` | no |
| `costPerHour` | body | `number` | no |
| `costPerHourValidFrom` | body | `date` | no |
| `costRates[]` | body | `array<object>` | no |
