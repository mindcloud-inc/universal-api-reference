# Update Invoice with BigCommerce (B2B)

## Endpoint

- **Method:** `PUT`
- **Path:** `ip/invoices/:invoiceId`
- **Base URL:** `https://api-b2b.bigcommerce.com/api/v3/io/`
- **Official documentation:** [Update Invoice](https://developer.bigcommerce.com/b2b-edition/apis/rest-management/invoice-management/invoice#create-invoice)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `details.details.lineItems[]` | body | `array` | no |
| `details.details.lineItems[].sku` | body | `string` | no |
| `details.details.lineItems[].unitPrice.code` | body | `string` | no |
| `dueDate` | body | `number` | no |
| `originalBalance.code` | body | `string` | no |
| `details.details` | body | `object` | no |
| `details.details.lineItems[].quantity` | body | `string` | no |
| `details.details.lineItems[].unitPrice.value` | body | `string` | no |
| `openBalance.code` | body | `string` | no |
| `openBalance.value` | body | `number` | no |
| `originalBalance.value` | body | `number` | no |
| `status` | body | `number` | no |
| `details.details.lineItems[].unitPrice` | body | `object` | no |
| `openBalance` | body | `object` | no |
| `details.details.lineItems[].description` | body | `string` | no |
| `originalBalance` | body | `object` | no |
| `details` | body | `object` | no |
| `details.details.lineItems[].comments` | body | `string` | no |
| `customerId` | body | `string` | no |
| `invoiceId` | path | `string` | yes |
| `purchaseOrderNumber` | body | `string` | no |
| `externalPdfUrl` | body | `string` | no |
| `termsConditions` | body | `string` | no |
| `externalId` | body | `string` | no |
