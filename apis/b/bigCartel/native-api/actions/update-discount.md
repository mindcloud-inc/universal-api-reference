# Update Discount with Big Cartel

Updates an existing discount in Big Cartel.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/v1/accounts/[:account-id]/discounts/[:discount-id]`
- **Base URL:** `https://api.bigcartel.com`
- **Official documentation:** [Update Discount](https://developers.bigcartel.com/api/v1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `account-id` | path | `number` | yes | The Big Cartel account ID. |
| `discount-id` | path | `string` | yes | The Big Cartel discount ID. |
| `data.id` | body | `string` | yes | — |
| `data.attributes.name` | body | `string` | yes | — |
| `data.attributes.code` | body | `string` | yes | — |
| `data.attributes.requirement_type` | body | `string` | yes | — |
| `data.attributes.expiration_type` | body | `string` | yes | — |
| `data.attributes.reward_type` | body | `string` | yes | — |
| `data.attributes.application_type` | body | `string` | yes | — |
| `data.attributes.percent_discount` | body | `number` | yes | — |
