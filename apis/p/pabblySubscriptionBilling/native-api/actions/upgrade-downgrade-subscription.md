# Upgrade Downgrade Subscription with Pabbly Subscription Billing

## Endpoint

- **Method:** `PUT`
- **Path:** `/v1/subscription/:subscriptionId/upgrade-downgrade`
- **Base URL:** `https://payments.pabbly.com/api`
- **Official documentation:** [Upgrade Downgrade Subscription](https://apidocs.pabbly.com/#f38eb77a-8284-4847-b8c0-debbda138399)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `activated_at_val` | body | `string` | no |
| `addons` | body | `string` | no |
| `card_id` | body | `string` | no |
| `coupon_code` | body | `string` | no |
| `customer_id` | body | `string` | no |
| `payment_mode` | body | `string` | no |
| `payment_term` | body | `string` | no |
| `plan_id` | body | `string` | no |
| `price` | body | `string` | no |
| `quantity` | body | `string` | no |
| `setup_fee` | body | `string` | no |
| `subscription_id` | path | `string` | no |
| `update_reason` | body | `string` | no |
