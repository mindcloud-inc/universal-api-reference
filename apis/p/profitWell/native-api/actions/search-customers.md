# Search Customers with ProfitWell

Finds customers in ProfitWell.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/customers/`
- **Base URL:** `https://api.profitwell.com`
- **Official documentation:** [Search Customers](https://classic.paddle.com/profitwell/)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `start_date` | query | `string` | no | Get customers who have been updated on or after this date. |
| `end_date` | query | `string` | no | Get customers who have been updated before this date. |
| `email` | query | `string` | no | Filter customers by email. |
| `direction` | query | `list` | no | Order the results ascending or descending. Accepted values: `asc`, `desc`. |
