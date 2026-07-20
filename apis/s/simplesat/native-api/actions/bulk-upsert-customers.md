# Bulk Upsert Customers with Simplesat

Creates or updates multiple customers in Simplesat.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/customers/bulk`
- **Base URL:** `https://api.simplesat.io`
- **Official documentation:** [Bulk Upsert Customers](https://developer.simplesat.io/api)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `customers[]` | body | `array<object>` | no |
