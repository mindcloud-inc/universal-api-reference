# Export Ratings with Customer.guru

Retrieves customer ratings from Customer.guru.

## Endpoint

- **Method:** `GET`
- **Path:** `/export/ratings`
- **Base URL:** `https://customer.guru`
- **Official documentation:** [Export Ratings](https://customer.guru/api/documentation/v2)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `page` | query | `number` | no | Zero-based export page number. |
| `per_page` | query | `number` | no | Number of rows to export per page. |
