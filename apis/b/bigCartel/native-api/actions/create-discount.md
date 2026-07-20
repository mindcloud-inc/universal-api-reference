# Create Discount with Big Cartel

Creates a discount in Big Cartel.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/accounts/[:account-id]/discounts`
- **Base URL:** `https://api.bigcartel.com`
- **Official documentation:** [Create Discount](https://developers.bigcartel.com/api/v1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `account-id` | path | `number` | yes | The Big Cartel account ID. |
| `data.attributes.name` | body | `string` | yes | — |
| `data.attributes.code` | body | `string` | yes | — |
| `data.attributes.requirement_type` | body | `string` | yes | — |
| `data.attributes.expiration_type` | body | `string` | yes | — |
| `data.attributes.reward_type` | body | `string` | yes | — |
| `data.attributes.application_type` | body | `string` | yes | — |
| `data.attributes.percent_discount` | body | `number` | yes | — |
