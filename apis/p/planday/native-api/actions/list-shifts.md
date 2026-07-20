# List Shifts with Planday

Retrieves a list of shifts from Planday.

## Endpoint

- **Method:** `GET`
- **Path:** `/scheduling/v1.0/shifts`
- **Base URL:** `https://openapi.planday.com`
- **Official documentation:** [List Shifts](https://openapi.planday.com/api/schedule/)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `CreatedFrom` | query | `date` | no |
| `CreatedTo` | query | `date` | no |
| `DepartmentId[]` | query | `array<number>` | no |
| `EmployeeGroupId[]` | query | `array<number>` | no |
| `EmployeeId[]` | query | `array<number>` | no |
| `From` | query | `string` | no |
| `Limit` | query | `number` | no |
| `ModifiedFrom` | query | `date` | no |
| `ModifiedTo` | query | `date` | no |
| `Offset` | query | `number` | no |
| `PositionId[]` | query | `array<number>` | no |
| `ShiftStatus` | query | `string` | no |
| `ShiftTypeId[]` | query | `array<number>` | no |
| `To` | query | `string` | no |
