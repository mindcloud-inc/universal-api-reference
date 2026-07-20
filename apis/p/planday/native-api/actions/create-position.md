# Create Position with Planday

Creates a new position in Planday.

## Endpoint

- **Method:** `POST`
- **Path:** `/scheduling/v1.0/positions`
- **Base URL:** `https://openapi.planday.com`
- **Official documentation:** [Create Position](https://openapi.planday.com/api/schedule/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `affectRevenue` | body | `boolean` | yes |
| `color` | body | `string` | no |
| `departmentId` | body | `number` | yes |
| `employeeGroupId` | body | `number` | yes |
| `name` | body | `string` | yes |
| `revenueUnitId` | body | `number` | no |
| `sectionId` | body | `number` | no |
| `skillIds[]` | body | `array<number>` | no |
| `validFrom` | body | `date` | no |
| `validTo` | body | `date` | no |
