# Create Customer With Subscription with Pabbly Subscription Billing

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/subscription`
- **Base URL:** `https://payments.pabbly.com/api`
- **Official documentation:** [Create Customer With Subscription](https://apidocs.pabbly.com/#fa365f13-a67c-4973-8967-0e4db2c2a109)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `addons` | body | `string` | no | Addons. |
| `card_number` | body | `string` | no | Pabbly Card Number. |
| `city` | body | `string` | no | Pabbly City. |
| `country` | body | `string` | no | Pabbly Country. |
| `coupon_code` | body | `string` | no | Pabbly Coupon Code. |
| `cvv` | body | `string` | no | Pabbly CVV. |
| `email` | body | `string` | no | Pabbly Email. |
| `first_name` | body | `string` | no | Pabbly First Name. |
| `gateway_id` | body | `string` | no | Unique Id of the payment gateway from which the payment is processed. |
| `gateway_type` | body | `string` | no | One of paypal, stripe, test, custom, connect, offline, or free. |
| `is_affiliate` | body | `string` | no | To create this customer as a Affiliate, it can be boolean value true or false. |
| `last_name` | body | `string` | no | Pabbly Last Name. |
| `month` | body | `string` | no | Pabbly Month. |
| `plan_amount` | body | `string` | no | Enter only the plan amount without adding the currency symbol. |
| `plan_id` | body | `string` | no | Unique Id of the plan which you will assign to this customer. |
| `quantity` | body | `string` | no | Quantity of the plan. |
| `redirect_to` | body | `string` | no | The customer will be redirected to this link after successful payment. |
| `state` | body | `string` | no | Pabbly State. |
| `street` | body | `string` | no | Pabbly Street. |
| `tax_id` | body | `string` | no | Tax ID recorded for a customer. |
| `year` | body | `string` | no | Pabbly Year. |
| `zip_code` | body | `string` | no | Pabbly Zip Code. |
