# List Leave Types with actiTIME

Retrieves a list of leave types from actiTIME.

## Endpoint

- **Method:** `GET`
- **Path:** `/leaveTypes`
- **Base URL:** `{instanceUrl}/api/v1`
- **Official documentation:** [List Leave Types](https://www.actitime.com/api-documentation/leave-types-resource)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `archived` | query | `boolean` | no | Filter archived vs active leave types. |
| `balance` | query | `string` | no | Balance filter value. |
| `ids` | query | `string` | no | Comma-separated leave type ids to be returned. |
| `name` | query | `string` | no | Exact leave type name match, case-insensitive. |
| `sort` | query | `string` | no | Sorting tokens like +name or -name. |
| `words` | query | `string` | no | Return leave types containing all given words in the name. |
