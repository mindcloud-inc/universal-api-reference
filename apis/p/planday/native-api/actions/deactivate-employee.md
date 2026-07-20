# Deactivate Employee with Planday

Deactivates an existing employee in Planday.

## Endpoint

- **Method:** `PUT`
- **Path:** `/hr/v1.0/employees/deactivate/:employeeId`
- **Base URL:** `https://openapi.planday.com`
- **Official documentation:** [Deactivate Employee](https://openapi.planday.com/api/hr/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `date` | body | `string` | no |
| `employeeId` | path | `number` | yes |
| `keepShifts` | body | `boolean` | no |
| `reason` | body | `string` | no |
