# Create Employee with Simplicate

## Endpoint

- **Method:** `POST`
- **Path:** `/hrm/employee`
- **Base URL:** `https://{subdomain}/api/v2`
- **Official documentation:** [Create Employee](https://developer.simplicate.com/docs/api/v2/reference/create-hrm-employee/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `person_id` | body | `string` | yes | Person identifier to convert into an employee. |
| `supervisor` | body | `object` | yes | Supervisor object with an employee id. |
| `status` | body | `object` | yes | Employee status object with an id. |
