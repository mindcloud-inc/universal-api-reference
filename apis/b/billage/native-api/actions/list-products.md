# List Products with Billage

Retrieves product records from Billage by alias or name.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/products`
- **Base URL:** `https://app.getbillage.com/api`
- **Official documentation:** [List Products](https://app.getbillage.com/api/documentation.html#/Products/productsByParameters)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `q` | query | `string` | no | Search products |
| `status` | query | `string` | no | Product status |
| `usage` | query | `string` | no | Product usage |
| `family` | query | `string` | no | Product family |
| `date-from` | query | `date` | no | Date from (yyyy-MM-dd) |
| `date-to` | query | `date` | no | Date to (yyyy-MM-dd) |
