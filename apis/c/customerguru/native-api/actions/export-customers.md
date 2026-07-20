# Export Customers with Customer.guru

Retrieves customers from Customer.guru.

## Endpoint

- **Method:** `GET`
- **Path:** `/export/customers`
- **Base URL:** `https://customer.guru`
- **Official documentation:** [Export Customers](https://customer.guru/api/documentation/v2#receiving)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `page` | query | `number` | no | Zero-based export page number. |
| `per_page` | query | `number` | no | Number of rows to export per page. |
