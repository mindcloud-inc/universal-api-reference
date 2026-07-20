# Update Employee with MyHR

## Endpoint

- **Method:** `PUT`
- **Path:** `/employees/:employee_pid`
- **Base URL:** `https://mindcloud.myhr.lu/api/v2`
- **Official documentation:** [Update Employee](https://www.postman.com/myhr-api/request/27799381-37025b1d-f6d9-405d-8071-dc99a24feb86)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `employee_pid` | path | `string` | yes | The employee PID. |
| `internal_number` | body | `string` | no | Updated internal employee number. |
| `person.first_name` | body | `string` | no | Updated employee first name. |
| `person.usual_name` | body | `string` | no | Updated employee last name. |
| `person.work_email` | body | `string` | no | Updated employee work email. |
