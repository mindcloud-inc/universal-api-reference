# Create Recurring Payment Link with Payfunnels

Creates a recurring payment link in Payfunnels.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/paymentlinks/recurring`
- **Base URL:** `https://api.payfunnels.com`
- **Official documentation:** [Create Recurring Payment Link](https://api.payfunnels.com/api/docs/#create-recurring-payment-link)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `title` | body | `string` | yes | Payment link title. |
| `description` | body | `string` | yes | Detailed description of the payment link. |
| `currencyCode` | body | `list` | no | ISO 4217 currency code for the payment link, for example USD or GBP. |
| `amount` | body | `number` | yes | Recurring payment amount. |
| `interval` | body | `string` | yes | Recurring interval. Supported values are day, week, month, and year. |
| `trialDays` | body | `number` | no | Optional trial period in days. Must be greater than 2 days. |
| `isTaxable` | body | `boolean` | no | Whether the default tax rate should be applied. |
| `forwardProcessingFees` | body | `boolean` | no | Whether processing fees should be added to the payment link. |
| `coupon[]` | body | `array<object>` | no | Optional coupon definitions to apply at checkout as an array of objects. |
| `displayBillingAddress` | body | `boolean` | no | Prompt the customer for a billing address. |
| `displayShippingAddress` | body | `boolean` | no | Prompt the customer for a shipping address. |
| `enableTermOfService` | body | `boolean` | no | Require the customer to accept terms of service. |
| `additionalFields[]` | body | `array<object>` | no | Additional checkout fields as an array of objects. |
| `oneTimeSetupFeeProductId` | body | `string` | no | Optional one-time setup fee product ID to include in the payment link. |
