# Update Employee with Craftboxx

Updates an employee in Craftboxx.

## Endpoint

- **Method:** `PUT`
- **Path:** `employees/:employeeId`
- **Base URL:** `https://api.craftboxx.de`
- **Official documentation:** [Update Employee](https://api.craftboxx.de/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | no | The employee email address. |
| `employeeId` | path | `number` | yes | The Craftboxx employee ID. |
| `first_name` | body | `string` | no | Employee first name. |
| `last_name` | body | `string` | no | Employee last name. |
| `inactive` | body | `boolean` | no | Whether the employee is inactive. |
