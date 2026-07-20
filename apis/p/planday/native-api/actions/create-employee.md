# Create Employee with Planday

Creates a new employee in Planday.

## Endpoint

- **Method:** `POST`
- **Path:** `/hr/v1.0/employees`
- **Base URL:** `https://openapi.planday.com`
- **Official documentation:** [Create Employee](https://openapi.planday.com/api/hr/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `departments[]` | body | `array<number>` | yes |
| `email` | body | `string` | no |
| `employeeGroups[]` | body | `array<number>` | no |
| `firstName` | body | `string` | yes |
| `jobTitle` | body | `string` | no |
| `lastName` | body | `string` | yes |
| `primaryDepartmentId` | body | `number` | no |
| `userName` | body | `string` | yes |
