# Get Time Off Policies for Employee with BambooHR

Retrieves time off policies for an employee from BambooHR.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/employees/:employeeId/time_off/policies`
- **Base URL:** `https://mindcloud.bamboohr.com/api`
- **Official documentation:** [Get Time Off Policies for Employee](https://documentation.bamboohr.com/reference/time-off-list-time-off-policies-for-employee-1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `employeeId` | path | `string` | yes | The BambooHR employee ID. |
