# Create One-Time Payment Link with Payfunnels

Creates a one-time payment link in Payfunnels.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/paymentlinks/onetime`
- **Base URL:** `https://api.payfunnels.com`
- **Official documentation:** [Create One-Time Payment Link](https://api.payfunnels.com/api/docs/#create-one-time-payment-link)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `title` | body | `string` | yes | Payment link title. |
| `description` | body | `string` | yes | Detailed description of the payment link. |
| `currencyCode` | body | `list` | no | ISO 4217 currency code for the payment link, for example USD or GBP. |
| `amount` | body | `number` | yes | One-time payment amount. |
| `isTaxable` | body | `boolean` | no | Whether the default tax rate should be applied. |
| `forwardProcessingFees` | body | `boolean` | no | Whether processing fees should be added to the payment link. |
| `coupon[]` | body | `array<object>` | no | Optional coupon definitions to apply at checkout as an array of objects. |
| `displayBillingAddress` | body | `boolean` | no | Prompt the customer for a billing address. |
| `displayShippingAddress` | body | `boolean` | no | Prompt the customer for a shipping address. |
| `enableTermOfService` | body | `boolean` | no | Require the customer to accept terms of service. |
| `additionalFields[]` | body | `array<object>` | no | Additional checkout fields as an array of objects. |
