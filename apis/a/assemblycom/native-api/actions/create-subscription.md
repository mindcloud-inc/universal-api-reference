# Create Subscription with Assembly.com

Creates a subscription in Assembly.com.

## Endpoint

- **Method:** `POST`
- **Path:** `/subscriptions`
- **Base URL:** `https://api.assembly.com/v1`
- **Official documentation:** [Create Subscription](https://docs.assembly.com/reference/create-subscription)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `clientId` | body | `string` | no | The ID of the client this subscription is assigned to. Leave empty if assigning to a company. |
| `companyId` | body | `string` | no | The ID of the company this subscription is assigned to. This is required when assigning to a company. |
| `templateId` | body | `string` | no | Unique ID of the invoice template to use. If provided, template values will be used for line items and invoice metadata. |
| `lineItems[]` | body | `array<object>` | no | Array of line items. Required if templateId is not provided. |
| `lineItems[].quantity` | body | `number` | yes | Quantity of the item (supports decimals). |
| `lineItems[].amount` | body | `number` | no | Amount in cents. Required if priceId is not provided. |
| `lineItems[].priceId` | body | `string` | no | Unique ID of the price object. Required if amount is not provided. |
| `lineItems[].description` | body | `string` | no | Description of the item, ignored if priceId is provided. |
| `memo` | body | `string` | no | Arbitrary string attached to the invoice, often used for display. |
| `daysUntilDue` | body | `number` | yes | The number of days from when the subscription invoice is created until it is due. Max value is 30. |
| `taxPercentage` | body | `number` | no | Tax percentage to apply to the invoice amount. |
| `interval` | body | `string` | no | Billing frequency. Required if line items do not include a recurring price. Values: day, week, month, quarterly, yearly. Accepted values: `0`, `1`, `2`, `3`, `4`. |
| `intervalCount` | body | `number` | no | Number of intervals between billings. Default value is 1. |
| `paymentMethodPreferences[]` | body | `array<object>` | yes | Array of preferences which specify which payment methods are allowed and how transaction fees are handled for each payment method. |
| `paymentMethodPreferences[].type` | body | `string` | yes | Payment method type. Values are creditCard or bankAccount. Accepted values: `0`, `1`. |
| `paymentMethodPreferences[].feePaidByClient` | body | `boolean` | yes | When true, the transaction fee is paid by the client, otherwise it is covered by your account. |
| `collectionMethod` | body | `string` | yes | Specify how to charge for an invoice. Values: sendInvoice or chargeAutomatically. Accepted values: `0`, `1`. |
