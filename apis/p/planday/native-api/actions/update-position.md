# Update Position with Planday

Updates an existing position in Planday.

## Endpoint

- **Method:** `PUT`
- **Path:** `/scheduling/v1.0/positions/:positionId`
- **Base URL:** `https://openapi.planday.com`
- **Official documentation:** [Update Position](https://openapi.planday.com/api/schedule/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `affectRevenue` | body | `boolean` | yes |
| `color` | body | `string` | no |
| `name` | body | `string` | yes |
| `positionId` | path | `number` | yes |
| `revenueUnitId` | body | `number` | no |
| `sectionId` | body | `number` | no |
| `skillIds[]` | body | `array<number>` | no |
| `validFrom` | body | `date` | no |
| `validTo` | body | `date` | no |
