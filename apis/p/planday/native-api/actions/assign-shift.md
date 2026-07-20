# Assign Shift with Planday

Assigns an employee to a shift in Planday.

## Endpoint

- **Method:** `POST`
- **Path:** `/scheduling/v1.0/shifts/:shiftId/employee`
- **Base URL:** `https://openapi.planday.com`
- **Official documentation:** [Assign Shift](https://openapi.planday.com/api/schedule/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `employeeId` | body | `number` | no |
| `shiftId` | path | `number` | yes |
