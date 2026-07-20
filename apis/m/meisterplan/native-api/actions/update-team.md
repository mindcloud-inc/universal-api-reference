# Update Team with Meisterplan

Updates an existing team in Meisterplan.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/teams/:teamId`
- **Base URL:** `https://api.us.meisterplan.com/v1`
- **Official documentation:** [Update Team](https://api.us.meisterplan.com/docs/api.html#operation/UpdateTeam)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `teamId` | path | `string` | yes |
| `resourceKey` | body | `string` | no |
| `name` | body | `string` | no |
| `primaryRole` | body | `object` | no |
| `obsUnits` | body | `object` | no |
| `skills[]` | body | `array<string>` | no |
| `resourceManager` | body | `object` | no |
| `costPerHour` | body | `number` | no |
| `costPerHourValidFrom` | body | `date` | no |
| `costRates[]` | body | `array<object>` | no |
| `standardBillingRatePerHour` | body | `number` | no |
| `velocity` | body | `object` | no |
