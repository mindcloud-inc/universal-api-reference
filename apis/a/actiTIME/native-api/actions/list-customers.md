# List Customers with actiTIME

Retrieves a list of customers from actiTIME.

## Endpoint

- **Method:** `GET`
- **Path:** `/customers`
- **Base URL:** `{instanceUrl}/api/v1`
- **Official documentation:** [List Customers](https://www.actitime.com/api-documentation/customers-resource)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `archived` | query | `boolean` | no | Filter archived vs active customers. |
| `ids` | query | `string` | no | Comma-separated ids of customers to be returned. |
| `name` | query | `string` | no | Exact customer name match, case-insensitive. |
| `sort` | query | `string` | no | Sorting tokens like +name or -created. |
| `words` | query | `string` | no | Return customers containing all given words in the name. |
