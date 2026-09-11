# Create Order with Peplink

## Endpoint

- **Method:** `POST`
- **Path:** `orders`
- **Base URL:** `https://portal.peplink.com/api/e/v1/cp/`

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `billingAddress` | body | `object` | no | Define a new billing address for this order. Make sure you set isUseDefaultBillingAddress to false when using new billing address. |
| `billingAddress.company` | body | `string` | no | — |
| `billingAddress.countryCode` | body | `string` | no | 2-char country code for this address. |
| `billingAddress.state` | body | `string` | no | — |
| `billingAddress.streetAddress` | body | `string` | no | — |
| `comment` | body | `string` | no | Add note for this order. |
| `customerEmail` | body | `string` | yes | Customer email to create the order. This should represent one of your users (seats) from your partner account. |
| `isUseDefaultBillingAddress` | body | `boolean` | no | true if to use the default billing address configured in eStore. false if you want to use a new billing address via billingAddress. |
| `orderItems[]` | body | `array` | yes | Ordered items in this order. Must contain at least one item. |
| `orderItems[].generateNewEsim` | body | `boolean` | no | Indicates if a new eSIM is needed to generate for the order item. Required if the order item is for generating new eSIM. |
| `orderItems[].iccids[]` | body | `array` | no | ICCIDs for the order item. Required if the order item is purchased for ICCIDs, e.g. data plan for eSIMs. |
| `orderItems[].quantity` | body | `number` | no | Defines how much quantity to purchase for the order item. Required if generateNewEsim is true. |
| `orderItems[].sku` | body | `string` | yes | SKU of the order item. |
| `paymentMethod` | body | `string` | no | Payment method for this order. Only payment terms PAYMENT_TERMS is supported now. |
| `billingAddress.city` | body | `string` | no | — |
| `isDryRun` | body | `boolean` | no | Set true if you want to test if your order is valid to create. false or leave it absent from the request if you want to create an actual order. |
| `couponCode` | body | `string` | no | Coupon code to apply discount to the order. |
| `orderItems[].serialNumbers[]` | body | `array<string>` | no | — |
| `billingAddress.zipCode` | body | `string` | no | — |
