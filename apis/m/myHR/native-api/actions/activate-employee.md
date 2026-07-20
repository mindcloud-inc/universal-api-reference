# Activate Employee with MyHR

## Endpoint

- **Method:** `POST`
- **Path:** `/hr/employees/:employee_pid/statuses/do/activate`
- **Base URL:** `https://mindcloud.myhr.lu/api/v2`
- **Official documentation:** [Activate Employee](https://www.postman.com/myhr-api/request/27799381-7598cfad-13d2-4a61-a46e-18f845daf442)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `comment` | body | `string` | no | Optional activation comment. |
| `date_effective` | body | `string` | yes | The activation effective date in YYYY-MM-DD format. |
| `employee_pid` | path | `string` | yes | The employee PID. |
