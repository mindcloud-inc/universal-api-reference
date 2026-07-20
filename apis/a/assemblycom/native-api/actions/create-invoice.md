# Create Invoice with Assembly.com

Creates an invoice in Assembly.com.

## Endpoint

- **Method:** `POST`
- **Path:** `/invoices`
- **Base URL:** `https://api.assembly.com/v1`
- **Official documentation:** [Create Invoice](https://docs.assembly.com/reference/create-invoice)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `clientId` | body | `string` | no | The ID of the client this invoice is assigned to. Leave empty if assigning to a company. |
| `companyId` | body | `string` | no | The ID of the company this invoice is assigned. This is required when an invoice is assigned to a company. |
| `templateId` | body | `string` | no | Unique ID of the invoice template to use. If provided, template values will be used for line items and invoice metadata. |
| `lineItems[]` | body | `array<object>` | no | Array of line items. Required if templateId is not provided. |
| `lineItems[].quantity` | body | `number` | yes | Quantity of the item (supports decimals). |
| `lineItems[].amount` | body | `number` | no | Amount in cents. Required if priceId not provided. |
| `lineItems[].priceId` | body | `string` | no | Unique ID of the price object. Required if amount is not provided. |
| `lineItems[].description` | body | `string` | no | Description of the item, ignored if priceId is provided. |
| `memo` | body | `string` | no | Memo attached to the invoice. |
| `daysUntilDue` | body | `number` | yes | The number of days from when the invoice is created until it is due. Max value is 30. |
| `taxPercentage` | body | `number` | no | Tax percentage to apply to the invoice amount. |
| `paymentMethodPreferences[]` | body | `array<object>` | yes | Array of preferences which specify which payment methods are allowed and how transaction fees are handled for each payment method. |
| `paymentMethodPreferences[].type` | body | `string` | yes | Payment method type. Values are creditCard or bankAccount. Accepted values: `0`, `1`. |
| `paymentMethodPreferences[].feePaidByClient` | body | `boolean` | yes | When true, the transaction fee is paid by the client, otherwise it is covered by your account. |
