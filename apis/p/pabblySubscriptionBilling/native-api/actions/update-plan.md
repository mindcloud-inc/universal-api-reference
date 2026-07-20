# Update Plan with Pabbly Subscription Billing

## Endpoint

- **Method:** `PUT`
- **Path:** `/v1/plan/update/:planId`
- **Base URL:** `https://payments.pabbly.com/api`
- **Official documentation:** [Update Plan](https://apidocs.pabbly.com/#44a4f878-2940-4284-8bd5-3464d2848298)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `billing_cycle` | body | `string` | no |
| `billing_cycle_num` | body | `string` | no |
| `billing_period` | body | `string` | no |
| `billing_period_num` | body | `string` | no |
| `currency_code` | body | `string` | no |
| `failed_payment_gateway` | body | `string` | no |
| `failed_payment_gateway_array` | body | `string` | no |
| `gateways_array` | body | `string` | no |
| `meta_data` | body | `string` | no |
| `payment_gateway` | body | `string` | no |
| `payment_term` | body | `string` | no |
| `plan_active` | body | `string` | no |
| `plan_code` | body | `string` | no |
| `plan_description` | body | `string` | no |
| `plan_id` | path | `string` | no |
| `plan_name` | body | `string` | no |
| `plan_type` | body | `string` | no |
| `price` | body | `string` | no |
| `product_id` | body | `string` | no |
| `redirect_url` | body | `string` | no |
| `setup_fee` | body | `string` | no |
| `specific_keep_live` | body | `string` | no |
| `trial_amount` | body | `string` | no |
| `trial_period` | body | `string` | no |
| `trial_type` | body | `string` | no |
| `variable_increase_price` | body | `string` | no |
| `variable_max_price_amount` | body | `string` | no |
| `variable_period_num` | body | `string` | no |
| `variable_start_time` | body | `string` | no |
| `variable_type` | body | `string` | no |
