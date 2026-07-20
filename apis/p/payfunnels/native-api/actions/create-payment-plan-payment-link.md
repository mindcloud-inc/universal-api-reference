# Create Payment Plan Payment Link with Payfunnels

Creates a payment plan link in Payfunnels.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/paymentlinks/paymentplan`
- **Base URL:** `https://api.payfunnels.com`
- **Official documentation:** [Create Payment Plan Payment Link](https://api.payfunnels.com/api/docs/#create-payment-plan-payment-link)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `title` | body | `string` | yes | Payment link title. |
| `description` | body | `string` | yes | Detailed description of the payment link. |
| `currencyCode` | body | `list` | no | ISO 4217 currency code for the payment link, for example USD or GBP. |
| `amount` | body | `number` | yes | Payment plan amount. |
| `interval` | body | `string` | yes | Payment interval. Supported values are day, week, month, and year. |
| `numberOfPayments` | body | `number` | yes | Number of payments to collect before the subscription cancels. |
| `trialDays` | body | `number` | no | Optional trial period in days. Must be greater than 2 days. |
| `isTaxable` | body | `boolean` | no | Whether the default tax rate should be applied. |
| `forwardProcessingFees` | body | `boolean` | no | Whether processing fees should be added to the payment link. |
| `coupon[]` | body | `array<object>` | no | Optional coupon definitions to apply at checkout as an array of objects. |
| `displayBillingAddress` | body | `boolean` | no | Prompt the customer for a billing address. |
| `displayShippingAddress` | body | `boolean` | no | Prompt the customer for a shipping address. |
| `enableTermOfService` | body | `boolean` | no | Require the customer to accept terms of service. |
| `additionalFields[]` | body | `array<object>` | no | Additional checkout fields as an array of objects. |
| `oneTimeSetupFeeProductId` | body | `string` | no | Optional one-time setup fee product ID to include in the payment link. |
