# Remove Trait Category with ProfitWell

Deletes a trait category from ProfitWell.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/v2/customer_traits/category/`
- **Base URL:** `https://api.profitwell.com`
- **Official documentation:** [Remove Trait Category](https://classic.paddle.com/profitwell/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `category` | body | `string` | yes | The category to remove from every customer that has it. |
