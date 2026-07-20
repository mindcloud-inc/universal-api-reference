# Update Employee with BambooHR

Updates an existing employee in BambooHR.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/employees/:employeeId`
- **Base URL:** `https://mindcloud.bamboohr.com/api`
- **Official documentation:** [Update Employee](https://documentation.bamboohr.com/reference/update-employee-1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `employeeId` | path | `string` | yes | The BambooHR employee identifier to update. |
| `firstName` | body | `string` | no | Employee first name. |
| `lastName` | body | `string` | no | Employee last name. |
