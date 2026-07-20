# Create Pay What You Want Payment Link with Payfunnels

Creates a pay-what-you-want payment link in Payfunnels.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/paymentlinks/paywhatyouwant`
- **Base URL:** `https://api.payfunnels.com`
- **Official documentation:** [Create Pay What You Want Payment Link](https://api.payfunnels.com/api/docs/#create-pay-what-you-want-payment-link)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `title` | body | `string` | yes | Pay-what-you-want payment link title. |
| `description` | body | `string` | yes | Detailed description of the payment link. |
| `currencyCode` | body | `list` | no | ISO 4217 currency code for the payment link, for example USD or GBP. |
| `allowOneTime` | body | `boolean` | no | Whether one-time payments are allowed. The provider default is true. |
| `allowRecurring` | body | `boolean` | no | Whether recurring payments are allowed. The provider default is false. |
| `isTaxable` | body | `boolean` | no | Whether the default tax rate should be applied. |
| `forwardProcessingFees` | body | `boolean` | no | Whether processing fees should be added to the payment link. |
| `displayBillingAddress` | body | `boolean` | no | Prompt the customer for a billing address. |
| `displayShippingAddress` | body | `boolean` | no | Prompt the customer for a shipping address. |
| `enableTermOfService` | body | `boolean` | no | Require the customer to accept terms of service. |
| `additionalFields[]` | body | `array<object>` | no | Additional checkout fields as an array of objects. |
