# Get Employee with Planfix

Retrieves an employee from Planfix.

## Endpoint

- **Method:** `GET`
- **Path:** `/user/:id`
- **Base URL:** `{accountBaseUrl}/rest`
- **Official documentation:** [Get Employee](https://help.planfix.com/restapidocs/#/Employee/get-user-id)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Planfix employee identifier. |
| `fields` | query | `string` | no | Comma-delimited employee fields to return. |
