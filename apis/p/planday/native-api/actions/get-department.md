# Get Department with Planday

Retrieves an existing department from Planday.

## Endpoint

- **Method:** `GET`
- **Path:** `/hr/v1.0/departments/:id`
- **Base URL:** `https://openapi.planday.com`
- **Official documentation:** [Get Department](https://openapi.planday.com/api/hr/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `number` | yes |
| `includeDeleted` | query | `boolean` | no |
| `managedEmployeesOnly` | query | `boolean` | no |
