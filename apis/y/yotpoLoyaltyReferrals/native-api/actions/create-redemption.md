# Create Redemption with Yotpo Loyalty & Referrals

Creates a redemption in Yotpo Loyalty & Referrals.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v2/redemptions`
- **Base URL:** `https://loyalty.yotpo.com`
- **Official documentation:** [Create Redemption](https://loyaltyapi.yotpo.com/reference/create-redemption)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `redemption_option_id` | body | `number` | yes | Unique identifier of the redemption option being redeemed. |
| `customer_email` | body | `string` | no | Customer email address. Use one customer identifier for the redemption request. |
| `pos_account_id` | body | `string` | no | Customer identifier from your POS system. Use one customer identifier for the redemption request. |
| `phone_number` | body | `string` | no | Customer phone number in E.164 format. Use one customer identifier for the redemption request. |
| `customer_id` | body | `string` | no | Customer identifier from your system. Use one customer identifier for the redemption request. |
| `delay_points_deduction` | body | `boolean` | no | Only deduct points when the associated order is later received. |
| `currency` | body | `string` | no | Currency code to use when the account is configured for multi-currency. |
| `points_to_redeem` | body | `number` | no | Point amount to redeem for variable redemptions. |
