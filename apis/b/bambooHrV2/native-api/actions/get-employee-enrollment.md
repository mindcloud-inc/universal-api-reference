# Get Employee Enrollment with BambooHR

Retrieves employee enrollment from BambooHR.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/time-tracking/employees/:employeeId`
- **Base URL:** `https://{companyDomain}.bamboohr.com/api`
- **Official documentation:** [Get Employee Enrollment](https://documentation.bamboohr.com/reference/get-time-tracking-employee-enrollment)

## Requirements

- **OAuth scopes:** `time_tracking:employees`
- **scope:** `time_tracking:employees` — BambooHR documents these OAuth scopes for this endpoint; access also follows the connected user permissions.

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `employeeId` | path | `number` | yes | The employee ID. |
