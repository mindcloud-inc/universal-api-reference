# List Employee Verification Records for an Employee with BambooHR

Lists employee verification records for an employee from BambooHR.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/employee-verifications/employees/:employeeId`
- **Base URL:** `https://{companyDomain}.bamboohr.com/api`
- **Official documentation:** [List Employee Verification Records for an Employee](https://documentation.bamboohr.com/reference/list-employee-verifications-by-employee)

## Requirements

- **OAuth scopes:** `employee_verifications`
- **scope:** `employee_verifications` — BambooHR documents these OAuth scopes for this endpoint; access also follows the connected user permissions.

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `employeeId` | path | `number` | yes | The internal employee ID of the employee whose verification history is returned. |
