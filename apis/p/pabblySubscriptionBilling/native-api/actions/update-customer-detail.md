# Update Customer Detail with Pabbly Subscription Billing

## Endpoint

- **Method:** `PUT`
- **Path:** `/v1/customer/:customerId`
- **Base URL:** `https://payments.pabbly.com/api`
- **Official documentation:** [Update Customer Detail](https://apidocs.pabbly.com/#5642ea4b-3e4f-4305-9031-ca7d4f563131)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `billing_address` | body | `string` | no | Update the billing address of the customer. |
| `company_name` | body | `string` | no | Update the Customer's company name. |
| `customer_id` | path | `string` | no | Pabbly Customer ID. |
| `enable_affiliate` | body | `string` | no | Value will be yes/no |
| `enable_portal` | body | `string` | no | Value will be yes/no |
| `first_name` | body | `string` | no | Update the First Name of your customer. |
| `last_name` | body | `string` | no | Update the Last Name of your customer. |
| `phone` | body | `string` | no | Update the Customer's phone number. |
| `shipping_address` | body | `string` | no | Update the shipping address of the customer. |
| `website` | body | `string` | no | Update the Customer's website name. |
