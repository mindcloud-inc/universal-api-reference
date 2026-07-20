# List Retain Unsubscribed Customers with ProfitWell

Retrieves Retain unsubscribed customers from ProfitWell.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/retain/unsubscribed_customers/:intervention_type/`
- **Base URL:** `https://api.profitwell.com`
- **Official documentation:** [List Retain Unsubscribed Customers](https://classic.paddle.com/profitwell/)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `intervention_type` | path | `list` | yes | Must be either term_optimization or reactivation. Accepted values: `reactivation`, `term_optimization`. |
| `start_date` | query | `string` | no | Get customers who unsubscribed on this date or later. |
| `end_date` | query | `string` | no | Get customers who unsubscribed on this date or before. |
