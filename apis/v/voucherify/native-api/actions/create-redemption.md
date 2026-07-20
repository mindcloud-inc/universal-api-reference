# Create Redemption with Voucherify

Creates a redemption in Voucherify.

## Endpoint

- **Method:** `POST`
- **Path:** `/redemptions`
- **Base URL:** `https://us1.api.voucherify.io/v1`
- **Official documentation:** [Create Redemption](https://docs.voucherify.io/api-reference/redemptions)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `order.amount` | body | `number` | yes |
| `redeemables[]` | body | `array<object>` | yes |
