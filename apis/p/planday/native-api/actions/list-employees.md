# List Employees with Planday

Retrieves a list of employees from Planday.

## Endpoint

- **Method:** `GET`
- **Path:** `/hr/v1.0/employees`
- **Base URL:** `https://openapi.planday.com`
- **Official documentation:** [List Employees](https://openapi.planday.com/api/hr/)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `createdFrom` | query | `date` | no |
| `createdTo` | query | `date` | no |
| `includeSecurityGroups` | query | `boolean` | no |
| `limit` | query | `number` | no |
| `modifiedFrom` | query | `date` | no |
| `modifiedTo` | query | `date` | no |
| `offset` | query | `number` | no |
| `searchQuery` | query | `string` | no |
| `special[]` | query | `array<string>` | no |
