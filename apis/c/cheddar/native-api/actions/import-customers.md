# Import Customers with Cheddar

Imports existing customer records into Cheddar.

## Endpoint

- **Method:** `POST`
- **Path:** `/customers/import/productCode/{productCode}`
- **Base URL:** `https://getcheddar.com/xml`
- **Official documentation:** [Import Customers](https://docs.getcheddar.com/#import-customers)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `code` | body | `string` | yes | Unique code for the customer in Cheddar. |
| `firstName` | body | `string` | yes | Customer first name. |
| `lastName` | body | `string` | yes | Customer last name. |
| `email` | body | `string` | yes | Customer email address. |
| `subscription` | body | `object` | no | Subscription details for the imported customer. |
| `subscription[planCode]` | body | `string` | yes | Pricing plan code to subscribe the customer to. |
| `subscription[method]` | body | `string` | no | Payment method: cc (default) or paypal. |
| `subscription[gatewayToken]` | body | `string` | no | Pre-tokenized payment method reference. |
| `subscription[couponCode]` | body | `string` | no | Promotion coupon code to apply. |
| `remoteAddress` | body | `string` | no | Client IPv4 address for fraud protection and rate limiting. |
