# Create Person with 4HSE

Creates a new person in 4HSE.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/person/create`
- **Base URL:** `https://service.4hse.com`
- **Official documentation:** [Create Person](https://docs.4hse.com/en/api/person/#operation-createPerson-post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `first_name` | body | `string` | yes | First name. Maximum length: 70. |
| `last_name` | body | `string` | yes | Last name. Maximum length: 70. |
| `project_id` | body | `string` | yes | Project (company) ID. |
| `code` | body | `string` | no | Employee code. Maximum length: 50. |
| `tax_code` | body | `string` | no | Tax code. Maximum length: 30. |
| `is_employee` | body | `number` | no | 1 for employee, 0 otherwise. |
| `unique_code` | body | `boolean` | no | Update existing person when code already exists. |
