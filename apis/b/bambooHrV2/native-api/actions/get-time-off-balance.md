# Get Time Off Balance with BambooHR

Retrieves an employee's time off balances from BambooHR.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/employees/:employeeId/time_off/calculator`
- **Base URL:** `https://mindcloud.bamboohr.com/api`
- **Official documentation:** [Get Time Off Balance](https://documentation.bamboohr.com/reference/time-off-get-time-off-balance)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `employeeId` | path | `string` | yes | The BambooHR employee ID. |
