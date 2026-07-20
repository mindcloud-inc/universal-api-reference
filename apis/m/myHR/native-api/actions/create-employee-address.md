# Create Employee Address with MyHR

## Endpoint

- **Method:** `POST`
- **Path:** `/hr/employees/:employee_pid/addresses`
- **Base URL:** `https://mindcloud.myhr.lu/api/v2`
- **Official documentation:** [Create Employee Address](https://www.postman.com/myhr-api/request/27799381-fae7a3d8-b769-43b9-b00b-91a098eaf06a)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `city` | body | `string` | yes | The city name. |
| `comment` | body | `string` | no | Optional comment for the address record. |
| `country_code` | body | `string` | yes | The 2-letter country code. |
| `date_effective` | body | `string` | yes | The date the address becomes effective in YYYY-MM-DD format. |
| `employee_pid` | path | `string` | yes | The employee PID. |
| `number` | body | `string` | yes | The street number. |
| `street` | body | `string` | yes | The street name. |
| `zipcode` | body | `string` | yes | The ZIP or postal code. |
