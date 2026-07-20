# Create Employee Time Off Request with MyHR

## Endpoint

- **Method:** `POST`
- **Path:** `/employees/:employee_pid/employee_timeoff_request`
- **Base URL:** `https://mindcloud.myhr.lu/api/v2`
- **Official documentation:** [Create Employee Time Off Request](https://www.postman.com/myhr-api/request/27799381-f56798cd-2a03-4638-9ff6-5b05b4034bca)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `employee_pid` | path | `string` | yes | The employee PID to create the time off request for. |
| `company_timeoff_reason.pid` | body | `string` | yes | The company time off reason PID to apply to the request. |
| `employee_timeoff_request_days[].date` | body | `string` | yes | The date for one requested time off day in YYYY-MM-DD format, for example 2026-03-31. |
| `employee_timeoff_request_days[].num_hours` | body | `number` | yes | The number of hours requested for one time off day, for example 8. |
| `status` | body | `string` | yes | The initial time off request status tag, for example TO_REVIEW. |
