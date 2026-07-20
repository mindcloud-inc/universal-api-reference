# Update Employee with Planday

Updates an existing employee in Planday.

## Endpoint

- **Method:** `PUT`
- **Path:** `/hr/v1.0/employees/:employeeId`
- **Base URL:** `https://openapi.planday.com`
- **Official documentation:** [Update Employee](https://openapi.planday.com/api/hr/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `departments[]` | body | `array<number>` | no |
| `email` | body | `string` | no |
| `employeeGroups[]` | body | `array<number>` | no |
| `employeeId` | path | `number` | yes |
| `firstName` | body | `string` | no |
| `jobTitle` | body | `string` | no |
| `lastName` | body | `string` | no |
| `primaryDepartmentId` | body | `number` | no |
| `userName` | body | `string` | no |
| `useValidation` | query | `boolean` | no |
