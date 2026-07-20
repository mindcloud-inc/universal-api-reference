# Create Role with Meisterplan

Creates a new role in Meisterplan.

## Endpoint

- **Method:** `POST`
- **Path:** `/roles`
- **Base URL:** `https://api.us.meisterplan.com/v1`
- **Official documentation:** [Create Role](https://api.us.meisterplan.com/docs/api.html#operation/CreateRole)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `name` | body | `string` | yes |
| `externalId` | body | `string` | no |
| `costType` | body | `string` | no |
| `obsUnits` | body | `object` | no |
| `resourceManager` | body | `object` | no |
| `costPerHour` | body | `number` | no |
| `costPerHourValidFrom` | body | `date` | no |
| `costRates[]` | body | `array<object>` | no |
