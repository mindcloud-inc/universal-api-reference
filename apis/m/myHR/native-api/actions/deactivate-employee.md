# Deactivate Employee with MyHR

## Endpoint

- **Method:** `POST`
- **Path:** `/hr/employees/:employee_pid/statuses/do/deactivate`
- **Base URL:** `https://mindcloud.myhr.lu/api/v2`
- **Official documentation:** [Deactivate Employee](https://www.postman.com/myhr-api/request/27799381-e8ffa5f2-1172-4773-a96c-742e9edb6ba7)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `comment` | body | `string` | no | Optional deactivation comment. |
| `date_effective` | body | `string` | yes | The deactivation effective date in YYYY-MM-DD format. |
| `employee_pid` | path | `string` | yes | The employee PID. |
