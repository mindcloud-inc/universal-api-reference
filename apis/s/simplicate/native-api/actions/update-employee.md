# Update Employee with Simplicate

## Endpoint

- **Method:** `PUT`
- **Path:** `/hrm/employee/:id`
- **Base URL:** `https://{subdomain}/api/v2`
- **Official documentation:** [Update Employee](https://developer.simplicate.com/docs/api/v2/reference/update-hrm-employee/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Employee identifier. |
| `person_id` | body | `string` | yes | Employee person identifier. |
| `supervisor` | body | `object` | yes | Supervisor object with an employee id. |
| `status` | body | `object` | yes | Employee status object with an id. |
