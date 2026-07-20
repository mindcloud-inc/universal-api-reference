# Create Plan with Pabbly Subscription Billing

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/plan/create`
- **Base URL:** `https://payments.pabbly.com/api`
- **Official documentation:** [Create Plan](https://apidocs.pabbly.com/#039094b9-417b-4f79-9f6e-baa9fcf95074)

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
| `max_quantity` | body | `string` | no |
| `meta_data` | body | `string` | no |
| `min_quantity` | body | `string` | no |
| `payment_gateway` | body | `string` | no |
| `payment_term` | body | `string` | no |
| `plan_active` | body | `string` | no |
| `plan_code` | body | `string` | no |
| `plan_description` | body | `string` | no |
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
| `variable_start_time` | body | `string` | no |
| `variable_type` | body | `string` | no |
