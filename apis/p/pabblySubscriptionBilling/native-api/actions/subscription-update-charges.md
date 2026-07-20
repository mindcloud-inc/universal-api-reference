# Subscription Update Charges with Pabbly Subscription Billing

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/subscription/:subscriptionId/update_charges`
- **Base URL:** `https://payments.pabbly.com/api`
- **Official documentation:** [Subscription Update Charges](https://apidocs.pabbly.com/#91017921-1880-4c11-ae56-e728dff46d44)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `addons` | body | `string` | no |
| `coupon_code` | body | `string` | no |
| `plan_id` | body | `string` | no |
| `price` | body | `string` | no |
| `quantity` | body | `string` | no |
| `setup_fee` | body | `string` | no |
| `subscription_id` | path | `string` | no |
