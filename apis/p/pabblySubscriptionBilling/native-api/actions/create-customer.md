# Create Customer with Pabbly Subscription Billing

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/customer`
- **Base URL:** `https://payments.pabbly.com/api`
- **Official documentation:** [Create Customer](https://apidocs.pabbly.com/#cde44e73-4f9d-44bc-be76-358c3a1633d7)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `billing_address` | body | `string` | no | Pabbly Billing Address. |
| `company_name` | body | `string` | no | Pabbly Company Name. |
| `email_id` | body | `string` | no | Email address of your customer. |
| `first_name` | body | `string` | no | First Name of your customer |
| `is_affiliate` | body | `string` | no | To create this customer as a Affiliate, It can be boolean value true or false |
| `last_name` | body | `string` | no | Last Name of your customer. |
| `phone` | body | `string` | no | Pabbly Phone. |
| `shipping_address` | body | `string` | no | Pabbly Shipping Address. |
| `website` | body | `string` | no | Pabbly Website. |
