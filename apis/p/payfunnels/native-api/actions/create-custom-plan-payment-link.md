# Create Custom Plan Payment Link with Payfunnels

Creates a custom plan payment link in Payfunnels.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/paymentlinks/customplan`
- **Base URL:** `https://api.payfunnels.com`
- **Official documentation:** [Create Custom Plan Payment Link](https://api.payfunnels.com/api/docs/#create-custom-plan-payment-link)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `title` | body | `string` | yes | Custom plan payment link title. |
| `description` | body | `string` | yes | Detailed description of the payment link. |
| `currencyCode` | body | `list` | no | ISO 4217 currency code for the payment link, for example USD or GBP. |
| `amount` | body | `number` | yes | Amount charged immediately when the custom plan payment link is used. |
| `paymentSchedule` | body | `object` | yes | Payment schedule object containing chargePhases and finalChargePhase. |
| `isTaxable` | body | `boolean` | no | Whether the default tax rate should be applied. |
| `forwardProcessingFees` | body | `boolean` | no | Whether processing fees should be added to the payment link. |
| `displayBillingAddress` | body | `boolean` | no | Prompt the customer for a billing address. |
| `displayShippingAddress` | body | `boolean` | no | Prompt the customer for a shipping address. |
| `enableTermOfService` | body | `boolean` | no | Require the customer to accept terms of service. |
| `additionalFields[]` | body | `array<object>` | no | Additional checkout fields as an array of objects. |
