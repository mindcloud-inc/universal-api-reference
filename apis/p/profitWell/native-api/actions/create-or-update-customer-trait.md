# Create Or Update Customer Trait with ProfitWell

Creates or updates a customer trait in ProfitWell.

## Endpoint

- **Method:** `PUT`
- **Path:** `/v2/customer_traits/trait/`
- **Base URL:** `https://api.profitwell.com`
- **Official documentation:** [Create Or Update Customer Trait](https://classic.paddle.com/profitwell/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customer_id` | body | `string` | no | The customer ID to add or update a trait for. |
| `email` | body | `string` | no | The customer email to add or update a trait for. Applies to all customers with this email. |
| `category` | body | `string` | yes | The trait category. |
| `trait` | body | `string` | yes | The trait value. |
