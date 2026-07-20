# Create Buy URL with Digistore24

Creates a customized buy URL in Digistore24.

## Endpoint

- **Method:** `POST`
- **Path:** `/createBuyUrl`
- **Base URL:** `https://www.digistore24.com/api/call`
- **Official documentation:** [Create Buy URL](https://digistore24.com/api/docs/paths/createBuyUrl.yaml)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `product_id` | query | `string` | yes | Product ID |
| `buyer` | query | `object` | no | Buyer object |
| `buyer.email` | query | `string` | no | — |
| `buyer.salutation` | query | `string` | no | — |
| `buyer.title` | query | `string` | no | — |
| `buyer.last_name` | query | `string` | no | — |
| `buyer.first_name` | query | `string` | no | — |
| `buyer.company` | query | `string` | no | — |
| `buyer.street` | query | `string` | no | — |
| `buyer.city` | query | `string` | no | — |
| `buyer.zipcode` | query | `string` | no | — |
| `buyer.state` | query | `string` | no | — |
| `buyer.country` | query | `string` | no | — |
| `buyer.phone_no` | query | `string` | no | — |
| `buyer.tax_id` | query | `string` | no | — |
| `buyer.readonly_keys` | query | `string` | no | — |
| `buyer.id` | query | `string` | no | — |
| `payment_plan` | query | `object` | no | Payment plan object |
| `payment_plan.first_amount` | query | `number` | no | — |
| `payment_plan.other_amounts` | query | `number` | no | — |
| `payment_plan.currency` | query | `string` | no | — |
| `payment_plan.number_of_installments` | query | `number` | no | — |
| `payment_plan.first_billing_interval` | query | `string` | no | — |
| `payment_plan.other_billing_intervals` | query | `string` | no | — |
| `payment_plan.test_interval` | query | `string` | no | — |
| `payment_plan.template` | query | `string` | no | — |
| `payment_plan.upgrade_order_id` | query | `string` | no | — |
| `payment_plan.upgrade_type` | query | `string` | no | — |
| `payment_plan.tax_mode` | query | `string` | no | — |
| `tracking` | query | `object` | no | Tracking object |
| `tracking.custom` | query | `string` | no | — |
| `tracking.affiliate` | query | `string` | no | — |
| `tracking.affiliate_priority` | query | `string` | no | — |
| `tracking.campaignkey` | query | `string` | no | — |
| `tracking.trackingkey` | query | `string` | no | — |
| `tracking.utm_source` | query | `string` | no | — |
| `tracking.utm_medium` | query | `string` | no | — |
| `tracking.utm_campaign` | query | `string` | no | — |
| `tracking.utm_term` | query | `string` | no | — |
| `tracking.utm_content` | query | `string` | no | — |
| `valid_until` | query | `string` | no | Validity end date/time |
| `urls` | query | `object` | no | Redirect URLs object |
| `urls.thankyou_url` | query | `string` | no | — |
| `urls.fallback_url` | query | `string` | no | — |
| `urls.upgrade_error_url` | query | `string` | no | — |
| `placeholders` | query | `object` | no | Placeholder replacements object |
| `settings` | query | `object` | no | Buy URL settings object |
| `settings.orderform_id` | query | `string` | no | — |
| `settings.affiliate_commission_rate` | query | `number` | no | — |
| `settings.affiliate_commission_fix` | query | `number` | no | — |
| `settings.voucher_code` | query | `string` | no | — |
| `settings.voucher_1st_rate` | query | `number` | no | — |
| `settings.voucher_oth_rates` | query | `number` | no | — |
| `settings.voucher_1st_amount` | query | `number` | no | — |
| `settings.voucher_oth_amounts` | query | `number` | no | — |
| `settings.force_rebilling` | query | `boolean` | no | — |
| `settings.pay_methods[]` | query | `array<string>` | no | — |
| `addons[]` | query | `array<object>` | no | Addon list |
| `addons[].product_id` | query | `string` | no | — |
| `addons[].first_amount` | query | `number` | no | — |
| `addons[].other_amounts` | query | `number` | no | — |
| `addons[].single_amount` | query | `number` | no | — |
| `addons[].default_quantity` | query | `number` | no | — |
| `addons[].max_quantity_type` | query | `string` | no | — |
| `addons[].max_quantity` | query | `number` | no | — |
| `addons[].currency` | query | `string` | no | Three-character currency code for the add-on. |
| `addons[].is_quantity_editable_before_purchase` | query | `string` | no | Whether the buyer can change the add-on quantity before purchase. |
| `addons[].is_quantity_editable_after_purchase` | query | `string` | no | Whether the buyer can change the add-on quantity after purchase. |
