# Create Shift with Planday

Creates a new shift in Planday.

## Endpoint

- **Method:** `POST`
- **Path:** `/scheduling/v1.0/shifts`
- **Base URL:** `https://openapi.planday.com`
- **Official documentation:** [Create Shift](https://openapi.planday.com/api/schedule/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `allowConflicts` | body | `boolean` | yes |
| `comment` | body | `string` | no |
| `date` | body | `string` | yes |
| `departmentId` | body | `number` | yes |
| `employeeGroupId` | body | `number` | yes |
| `employeeId` | body | `number` | no |
| `endTime` | body | `string` | no |
| `positionId` | body | `number` | no |
| `shiftTypeId` | body | `number` | no |
| `skillIds[]` | body | `array<number>` | no |
| `startTime` | body | `string` | no |
| `useBreaks` | body | `boolean` | yes |
