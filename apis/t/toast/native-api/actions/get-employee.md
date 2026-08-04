# Get Employee with Toast

Retrieves one employee by Toast GUID or external identifier.

## Endpoint

- **Method:** `GET`
- **Path:** `/labor/v1/employees/:employeeId`
- **Base URL:** `{connection}`
- **API:** Labor
- **Official documentation:** [Get Employee](https://doc.toasttab.com/openapi/labor/operation/employeesEmployeeIdGet/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `employeeId` | path | `string` | yes | The Toast GUID or external identifier of the employee. |
