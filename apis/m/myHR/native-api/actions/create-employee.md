# Create Employee with MyHR

## Endpoint

- **Method:** `POST`
- **Path:** `/employees`
- **Base URL:** `https://mindcloud.myhr.lu/api/v2`
- **Official documentation:** [Create Employee](https://www.postman.com/myhr-api/request/27799381-8fa91af3-bd8e-44aa-bfe8-c48a483ba055)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `hire_date` | body | `string` | yes | The employee hire date in YYYY-MM-DD format. |
| `internal_number` | body | `string` | no | Optional internal employee number. |
| `person.first_name` | body | `string` | yes | The employee first name. |
| `person.language` | body | `string` | yes | The employee language. |
| `person.usual_name` | body | `string` | yes | The employee last name. |
| `person.work_email` | body | `string` | yes | The employee work email. |
| `seniority_date` | body | `string` | yes | The employee seniority date in YYYY-MM-DD format. |
