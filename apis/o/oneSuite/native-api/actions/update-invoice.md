# Update Invoice with OneSuite

Updates an invoice in OneSuite.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/v1/invoices/:invoice_id`
- **Base URL:** `https://api.onesuite.io`
- **Official documentation:** [Update Invoice](https://rest-api.onesuite.io/#edit-invoice)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `address` | body | `string` | no | Your company address |
| `city` | body | `string` | no | Your company city |
| `createdDate` | body | `date` | no | Invoice create date |
| `email` | body | `string` | no | Your company email address |
| `invoice_id` | path | `string` | yes | Invoice ID |
| `invoiceItems[]` | body | `array<object>` | no | Invoice line items |
| `note` | body | `string` | no | Notes for the invoice |
| `phone` | body | `string` | no | Your company contact number |
| `postBoxNo` | body | `string` | no | Post box number |
| `street` | body | `string` | no | Your company street |
| `company` | body | `string` | yes | Your company name |
| `client.key` | body | `string` | yes | Client ID |
| `clientName` | body | `string` | yes | Client display name |
| `clientCompany` | body | `string` | yes | Client company name |
| `description` | body | `string` | yes | Invoice description |
| `subTotalPrice` | body | `number` | yes | Subtotal price |
| `salesTax` | body | `number` | yes | Sales tax amount |
| `totalPrice` | body | `number` | yes | Total price |
| `dueDate` | body | `date` | yes | Invoice due date |
| `currency` | body | `string` | yes | Currency code |
| `project.key` | body | `string` | no | Project ID |
| `name` | body | `string` | no | Invoice name |
| `invoiceNo` | body | `string` | yes | Invoice number |
