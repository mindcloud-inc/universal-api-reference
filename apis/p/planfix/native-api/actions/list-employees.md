# List Employees with Planfix

Retrieves employees from Planfix.

## Endpoint

- **Method:** `POST`
- **Path:** `/user/list`
- **Base URL:** `{accountBaseUrl}/rest`
- **Official documentation:** [List Employees](https://help.planfix.com/restapidocs/#/Employee/get-user-list)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `fields` | body | `string` | no | Comma-delimited employee fields to return. |
| `pageSize` | body | `number` | no | Number of employees to return. |
| `offset` | body | `number` | no | Employee list offset. |
| `onlyActive` | body | `boolean` | no | Return only active employees. |
