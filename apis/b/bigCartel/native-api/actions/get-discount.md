# Get Discount with Big Cartel

Retrieves a discount from Big Cartel.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/accounts/[:account-id]/discounts/[:discount-id]`
- **Base URL:** `https://api.bigcartel.com`
- **Official documentation:** [Get Discount](https://developers.bigcartel.com/api/v1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `account-id` | path | `number` | yes | The Big Cartel account ID. |
| `discount-id` | path | `string` | yes | The Big Cartel discount ID. |
