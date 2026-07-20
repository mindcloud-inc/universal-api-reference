# List Departments with actiTIME

Retrieves a list of departments from actiTIME.

## Endpoint

- **Method:** `GET`
- **Path:** `/departments`
- **Base URL:** `{instanceUrl}/api/v1`
- **Official documentation:** [List Departments](https://www.actitime.com/api-documentation/departments-resource)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | query | `string` | no | Exact department name match, case-insensitive. |
| `sort` | query | `string` | no | Sorting tokens like +name or -name. |
