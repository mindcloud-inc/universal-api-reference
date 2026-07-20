# Create Subscription For Existing Customer with Pabbly Subscription Billing

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/subscription/:customerId`
- **Base URL:** `https://payments.pabbly.com/api`
- **Official documentation:** [Create Subscription For Existing Customer](https://apidocs.pabbly.com/#6143db10-efd1-42f9-91da-0ced427e871f)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `addons` | body | `string` | no | Addons. |
| `card_number` | body | `string` | no | Pabbly Card Number. |
| `coupon_code` | body | `string` | no | Coupon code to add to this subscription. |
| `customer_id` | path | `string` | no | Pabbly Customer ID. |
| `cvv` | body | `string` | no | Pabbly CVV. |
| `gateway_id` | body | `string` | no | Gateway id when multiple payment gateways of the same kind exist. |
| `gateway_type` | body | `string` | no | One of paypal, stripe, test, custom, connect, offline, or free. |
| `method_id` | body | `string` | no | Payment method id for charging from an existing or specific card. |
| `month` | body | `string` | no | Pabbly Month. |
| `plan_amount` | body | `string` | no | Enter only the plan amount without adding the currency symbol. |
| `plan_id` | body | `string` | no | Unique Id of the plan which you will assign to this customer. |
| `quantity` | body | `string` | no | Quantity of the plan. |
| `redirect_to` | body | `string` | no | The customer will be redirected to this link after successful payment. |
| `tax_id` | body | `string` | no | Tax ID recorded for a customer. |
| `year` | body | `string` | no | Pabbly Year. |
