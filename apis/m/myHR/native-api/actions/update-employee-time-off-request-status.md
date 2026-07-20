# Update Employee Time Off Request Status with MyHR

## Endpoint

- **Method:** `PUT`
- **Path:** `/employee_timeoff_requests/:employee_timeoff_request_pid/status`
- **Base URL:** `https://mindcloud.myhr.lu/api/v2`
- **Official documentation:** [Update Employee Time Off Request Status](https://www.postman.com/myhr-api/request/27799381-0b37fc72-1f8f-47d8-8e35-4a0c1b1dcff9)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `employee_timeoff_request_pid` | path | `string` | yes | The employee time off request PID. |
| `status` | body | `string` | yes | The status tag to apply to the time off request, for example ACCEPTED. |
