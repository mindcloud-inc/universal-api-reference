# Create Customer with Cheddar

Creates a new customer and subscription in Cheddar.

## Endpoint

- **Method:** `POST`
- **Path:** `/customers/new/productCode/{productCode}`
- **Base URL:** `https://getcheddar.com/xml`
- **Official documentation:** [Create Customer](https://docs.getcheddar.com/#create-a-new-customer)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `code` | body | `string` | yes | Unique code for the customer in Cheddar. |
| `firstName` | body | `string` | yes | Customer first name. |
| `lastName` | body | `string` | yes | Customer last name. |
| `email` | body | `string` | yes | Customer email address. |
| `subscription` | body | `object` | no | Subscription details for the new customer. |
| `subscription[planCode]` | body | `string` | yes | Pricing plan code to subscribe the customer to. |
| `subscription[method]` | body | `string` | no | Payment method: cc (default) or paypal. |
| `subscription[ccNumber]` | body | `string` | no | Credit or debit card number when card payment details are provided. |
| `subscription[ccExpiration]` | body | `string` | no | Card expiration in MM/YYYY format. |
| `subscription[ccCardCode]` | body | `string` | no | Card verification code when required by the payment flow. |
| `subscription[gatewayToken]` | body | `string` | no | Pre-tokenized payment method reference. |
| `subscription[couponCode]` | body | `string` | no | Promotion coupon code to apply. |
| `remoteAddress` | body | `string` | no | Client IPv4 address for fraud protection and rate limiting. |
