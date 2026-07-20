# Create Team with Meisterplan

Creates a new team in Meisterplan.

## Endpoint

- **Method:** `POST`
- **Path:** `/teams`
- **Base URL:** `https://api.us.meisterplan.com/v1`
- **Official documentation:** [Create Team](https://api.us.meisterplan.com/docs/api.html#operation/CreateTeam)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `resourceKey` | body | `string` | no |
| `name` | body | `string` | yes |
| `primaryRole` | body | `object` | no |
| `obsUnits` | body | `object` | no |
| `skills[]` | body | `array<string>` | no |
| `resourceManager` | body | `object` | no |
| `costPerHour` | body | `number` | no |
| `costPerHourValidFrom` | body | `date` | no |
| `costRates[]` | body | `array<object>` | no |
| `standardBillingRatePerHour` | body | `number` | no |
| `velocity` | body | `object` | no |
