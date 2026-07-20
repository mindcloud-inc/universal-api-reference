# Create Embedded Reward with Giftbit

Creates an embedded Giftbit reward for immediate in-app delivery.

## Endpoint

- **Method:** `POST`
- **Path:** `/embedded`
- **Base URL:** `https://api-testbed.giftbit.com/papi/v1`
- **Official documentation:** [Create Embedded Reward](https://www.giftbit.com/api-documentation)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | body | `string` | yes |
| `brand_code` | body | `string` | yes |
| `price_in_cents` | body | `number` | yes |
