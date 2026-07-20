# List Customers with Eduzz

Retrieves customers from Eduzz using the provided filters.

## Endpoint

- **Method:** `GET`
- **Path:** `/myeduzz/v1/customers`
- **Base URL:** `https://api.eduzz.com`
- **Official documentation:** [List Customers](https://developers.eduzz.com/reference/api/get-myeduzz-v1-customers)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `endDate` | query | `string` | no | Include customers through this date. |
| `order` | query | `string` | no | Sort order string accepted by Eduzz for customer listing. |
| `startDate` | query | `string` | no | Include customers from this date onward. |
