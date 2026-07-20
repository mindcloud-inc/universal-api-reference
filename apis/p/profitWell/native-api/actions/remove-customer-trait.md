# Remove Customer Trait with ProfitWell

Deletes a customer trait from ProfitWell.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/v2/customer_traits/trait/`
- **Base URL:** `https://api.profitwell.com`
- **Official documentation:** [Remove Customer Trait](https://classic.paddle.com/profitwell/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customer_id` | body | `string` | no | The customer ID to remove a trait from. |
| `email` | body | `string` | no | The customer email to remove a trait from. Applies to all customers with this email. |
| `category` | body | `string` | yes | The trait category. |
| `trait` | body | `string` | yes | The trait value to remove. |
