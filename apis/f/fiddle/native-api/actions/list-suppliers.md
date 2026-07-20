# List Suppliers with Fiddle

Retrieves supplier records from the Fiddle account.

## Endpoint

- **Method:** `GET`
- **Path:** `/suppliers`
- **Base URL:** `https://fiddle.io/rest/api/v2`
- **Official documentation:** [List Suppliers](https://fiddle.io/rest/api/v2/docs/)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `page` | query | `number` | no | Page number |
| `size` | query | `number` | no | Page size |
| `query` | query | `string` | no | Supplier search query |
| `ids[]` | query | `array<string>` | no | Supplier IDs |
| `sortBy` | query | `string` | no | Sort field |
| `sortDirection` | query | `string` | no | Sort direction |
