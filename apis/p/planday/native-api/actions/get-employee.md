# Get Employee with Planday

Retrieves an existing employee from Planday.

## Endpoint

- **Method:** `GET`
- **Path:** `/hr/v1.0/employees/:employeeId`
- **Base URL:** `https://openapi.planday.com`
- **Official documentation:** [Get Employee](https://openapi.planday.com/api/hr/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `employeeId` | path | `number` | yes |
| `special[]` | query | `array<string>` | no |
