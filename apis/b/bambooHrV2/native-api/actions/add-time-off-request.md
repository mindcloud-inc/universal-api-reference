# Add Time Off Request with BambooHR

Creates a time off request for an employee in BambooHR.

## Endpoint

- **Method:** `PUT`
- **Path:** `/v1/employees/:employeeId/time_off/request`
- **Base URL:** `https://mindcloud.bamboohr.com/api`
- **Official documentation:** [Add Time Off Request](https://documentation.bamboohr.com/reference/time-off-add-a-time-off-request)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `employeeId` | path | `string` | yes | The BambooHR employee identifier for the time-off request. |
