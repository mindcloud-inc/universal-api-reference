# Create Employee with Craftboxx

Creates an employee in Craftboxx.

## Endpoint

- **Method:** `POST`
- **Path:** `employees`
- **Base URL:** `https://api.craftboxx.de`
- **Official documentation:** [Create Employee](https://api.craftboxx.de/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `first_name` | body | `string` | yes | Employee first name. |
| `last_name` | body | `string` | yes | Employee last name. |
| `email` | body | `string` | yes | The employee email address. |
