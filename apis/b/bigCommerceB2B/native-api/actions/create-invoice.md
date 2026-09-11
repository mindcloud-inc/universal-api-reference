# Create Invoice with BigCommerce (B2B)

## Endpoint

- **Method:** `POST`
- **Path:** `ip/invoices`
- **Base URL:** `https://api-b2b.bigcommerce.com/api/v3/io/`
- **Official documentation:** [Create Invoice](https://developer.bigcommerce.com/b2b-edition/apis/rest-management/invoice-management/invoice#create-invoice)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `dueDate` | body | `number` | no | — |
| `externalId` | body | `string` | no | — |
| `invoiceNumber` | body | `string` | yes | — |
| `termsConditions` | body | `string` | no | — |
| `details.details.lineItems[]` | body | `array` | no | — |
| `details.details.lineItems[].sku` | body | `string` | no | — |
| `details.details.lineItems[].unitPrice.code` | body | `string` | no | — |
| `extraFields[].fieldName` | body | `string` | no | — |
| `status` | body | `number` | no | — |
| `details.details` | body | `object` | no | — |
| `details.details.lineItems[].quantity` | body | `string` | no | — |
| `details.details.lineItems[].unitPrice.value` | body | `string` | no | — |
| `openBalance.code` | body | `string` | no | — |
| `openBalance.value` | body | `number` | no | — |
| `originalBalance` | body | `object` | no | — |
| `originalBalance.code` | body | `string` | no | — |
| `originalBalance.value` | body | `number` | no | — |
| `details.details.lineItems[].unitPrice` | body | `object` | no | — |
| `openBalance` | body | `object` | no | — |
| `details.details.lineItems[].description` | body | `string` | no | — |
| `issuedAt` | body | `number` | no | — |
| `details` | body | `object` | no | — |
| `details.details.lineItems[].comments` | body | `string` | no | — |
| `customerId` | body | `string` | no | — |
| `purchaseOrderNumber` | body | `string` | no | — |
| `extraFields[]` | body | `array` | no | — |
| `externalPdfUrl` | body | `string` | no | — |
| `orderNumber` | body | `string` | no | BigCommerce order ID associated with this invoice. |
| `extraFields[].fieldValue` | body | `string` | no | — |
