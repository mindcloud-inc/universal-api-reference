# Update Shift with Planday

Updates an existing shift in Planday.

## Endpoint

- **Method:** `PUT`
- **Path:** `/scheduling/v1.0/shifts/:shiftId`
- **Base URL:** `https://openapi.planday.com`
- **Official documentation:** [Update Shift](https://openapi.planday.com/api/schedule/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `allowConflicts` | body | `boolean` | yes |
| `date` | body | `string` | yes |
| `employeeGroupId` | body | `number` | yes |
| `employeeId` | body | `number` | no |
| `endTime` | body | `string` | no |
| `positionId` | body | `number` | no |
| `shiftId` | path | `number` | yes |
| `shiftTypeId` | body | `number` | no |
| `startTime` | body | `string` | no |
| `useBreaks` | body | `boolean` | yes |
