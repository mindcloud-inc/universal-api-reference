# Get Employee with BambooHR

Retrieves details for one employee from BambooHR.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/employees/:id`
- **Base URL:** `https://mindcloud.bamboohr.com/api`
- **Official documentation:** [Get Employee](https://documentation.bamboohr.com/reference/get-employee-1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The BambooHR employee identifier to retrieve from the employee path segment. |
| `fields` | query | `string` | no | Optional comma-separated BambooHR field IDs to return. Defaults to a useful employee summary set when left blank. |
