# List Employees with Toast

Retrieves employees for the connected restaurant, optionally limited to specific identifiers.

## Endpoint

- **Method:** `GET`
- **Path:** `/labor/v1/employees`
- **Base URL:** `{connection}`
- **API:** Labor
- **Official documentation:** [List Employees](https://doc.toasttab.com/openapi/labor/operation/employeesGet/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `employeeIds` | query | `string` | no | One or more Toast GUIDs or external employee identifiers, with a maximum of 100. Send multiple values as a array. |
