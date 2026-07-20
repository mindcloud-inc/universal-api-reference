# Reactivate Employee with Planday

Reactivates a deactivated employee in Planday.

## Endpoint

- **Method:** `PUT`
- **Path:** `/hr/v1.0/employees/reactivate/:employeeId`
- **Base URL:** `https://openapi.planday.com`
- **Official documentation:** [Reactivate Employee](https://openapi.planday.com/api/hr/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `comment` | body | `string` | no |
| `departments[]` | body | `array<number>` | no |
| `employeeId` | path | `number` | yes |
