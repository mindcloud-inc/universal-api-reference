# Terminate Employee with MyHR

## Endpoint

- **Method:** `POST`
- **Path:** `/hr/employees/:employee_pid/statuses/do/terminate`
- **Base URL:** `https://mindcloud.myhr.lu/api/v2`
- **Official documentation:** [Terminate Employee](https://www.postman.com/myhr-api/request/27799381-bf72dd47-8c68-45ea-844c-b82d8a0f418d)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `comment` | body | `string` | no | Optional termination comment. |
| `date_effective` | body | `string` | yes | The termination effective date in YYYY-MM-DD format. |
| `employee_pid` | path | `string` | yes | The employee PID. |
