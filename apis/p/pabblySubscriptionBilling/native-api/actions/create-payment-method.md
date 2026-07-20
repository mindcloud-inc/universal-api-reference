# Create Payment Method with Pabbly Subscription Billing

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/paymentmethod/:customerId`
- **Base URL:** `https://payments.pabbly.com/api`
- **Official documentation:** [Create Payment Method](https://apidocs.pabbly.com/#120f63aa-80f5-44e1-86c4-7d38ac07ed0a)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `card_number` | body | `string` | no |
| `city` | body | `string` | no |
| `country` | body | `string` | no |
| `customer_id` | path | `string` | no |
| `cvv` | body | `string` | no |
| `email` | body | `string` | no |
| `first_name` | body | `string` | no |
| `gateway_type` | body | `string` | no |
| `last_name` | body | `string` | no |
| `month` | body | `string` | no |
| `state` | body | `string` | no |
| `street` | body | `string` | no |
| `year` | body | `string` | no |
| `zip_code` | body | `string` | no |
