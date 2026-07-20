# Create Employee with BambooHR

Creates a new employee in BambooHR.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/employees`
- **Base URL:** `https://mindcloud.bamboohr.com/api`
- **Official documentation:** [Create Employee](https://documentation.bamboohr.com/reference/add-employee-2)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `firstName` | body | `string` | yes | The new employee's first name. |
| `lastName` | body | `string` | yes | The new employee's last name. |
