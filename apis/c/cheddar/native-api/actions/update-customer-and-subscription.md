# Update Customer and Subscription with Cheddar

Updates customer and subscription details in Cheddar.

## Endpoint

- **Method:** `POST`
- **Path:** `/customers/edit/productCode/{productCode}/code/:customerCode`
- **Base URL:** `https://getcheddar.com/xml`
- **Official documentation:** [Update Customer and Subscription](https://docs.getcheddar.com/#update-a-customer-and-subscription)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `code` | path | `string` | yes | Customer code from Cheddar. |
| `firstName` | body | `string` | no | Customer first name. |
| `lastName` | body | `string` | no | Customer last name. |
| `email` | body | `string` | no | Customer email address. |
| `subscription` | body | `object` | no | Subscription fields to update for the customer. |
| `subscription[planCode]` | body | `string` | no | Pricing plan code to set on the subscription. |
| `subscription[method]` | body | `string` | no | Payment method: cc or paypal. |
| `remoteAddress` | body | `string` | no | Client IPv4 address for fraud protection and rate limiting. |
