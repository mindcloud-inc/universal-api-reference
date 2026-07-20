# Delete Discount with Big Cartel

Deletes a discount from Big Cartel.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/v1/accounts/[:account-id]/discounts/[:discount-id]`
- **Base URL:** `https://api.bigcartel.com`
- **Official documentation:** [Delete Discount](https://developers.bigcartel.com/api/v1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `account-id` | path | `number` | yes | The Big Cartel account ID. |
| `discount-id` | path | `string` | yes | The Big Cartel discount ID. |
