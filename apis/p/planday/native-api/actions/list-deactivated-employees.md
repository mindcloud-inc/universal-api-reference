# List Deactivated Employees with Planday

Retrieves a list of deactivated employees from Planday.

## Endpoint

- **Method:** `GET`
- **Path:** `/hr/v1.0/employees/deactivated`
- **Base URL:** `https://openapi.planday.com`
- **Official documentation:** [List Deactivated Employees](https://openapi.planday.com/api/hr/)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `createdFrom` | query | `date` | no |
| `createdTo` | query | `date` | no |
| `deactivatedFrom` | query | `date` | no |
| `deactivatedTo` | query | `date` | no |
| `limit` | query | `number` | no |
| `modifiedFrom` | query | `date` | no |
| `modifiedTo` | query | `date` | no |
| `offset` | query | `number` | no |
| `searchQuery` | query | `string` | no |
| `special[]` | query | `array<string>` | no |
