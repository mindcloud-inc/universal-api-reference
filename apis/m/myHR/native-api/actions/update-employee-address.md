# Update Employee Address with MyHR

## Endpoint

- **Method:** `PATCH`
- **Path:** `/hr/employees/:employee_pid/addresses/:employee_address_pid`
- **Base URL:** `https://mindcloud.myhr.lu/api/v2`
- **Official documentation:** [Update Employee Address](https://www.postman.com/myhr-api/request/27799381-49d25de7-6945-4854-8731-a71d65269ac9)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `city` | body | `string` | no | Updated city name. |
| `country_code` | body | `string` | no | Updated 2-letter country code. |
| `employee_address_pid` | path | `string` | yes | The employee address PID. |
| `employee_pid` | path | `string` | yes | The employee PID. |
| `number` | body | `string` | no | Updated street number. |
| `street` | body | `string` | no | Updated street name. |
| `zipcode` | body | `string` | no | Updated ZIP or postal code. |
