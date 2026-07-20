# List Customers with Fiddle

Retrieves customer records from the Fiddle account.

## Endpoint

- **Method:** `GET`
- **Path:** `/customers`
- **Base URL:** `https://fiddle.io/rest/api/v2`
- **Official documentation:** [List Customers](https://fiddle.io/rest/api/v2/docs/)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `page` | query | `number` | no | Page number |
| `size` | query | `number` | no | Page size |
| `query` | query | `string` | no | Customer search query |
| `status` | query | `string` | no | Customer status filter |
| `sortBy` | query | `string` | no | Sort field |
| `sortDirection` | query | `string` | no | Sort direction |
