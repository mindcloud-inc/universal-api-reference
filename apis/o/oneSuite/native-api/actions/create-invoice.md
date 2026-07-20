# Create Invoice with OneSuite

Creates an invoice in OneSuite.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/invoices`
- **Base URL:** `https://api.onesuite.io`
- **Official documentation:** [Create Invoice](https://rest-api.onesuite.io/#create-invoice)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `address` | body | `string` | no | Your company address |
| `city` | body | `string` | no | Your company city |
| `company` | body | `string` | yes | Your company name |
| `createdDate` | body | `date` | no | Invoice create date |
| `email` | body | `string` | no | Your company email address |
| `invoiceItems[]` | body | `array<object>` | no | Invoice line items |
| `note` | body | `string` | no | Notes for the invoice |
| `phone` | body | `string` | no | Your company contact number |
| `postBoxNo` | body | `string` | no | Post box number |
| `street` | body | `string` | no | Your company street |
| `client.key` | body | `string` | yes | Client ID |
| `clientName` | body | `string` | yes | Client display name |
| `clientCompany` | body | `string` | yes | Client company name |
| `description` | body | `string` | yes | Invoice description |
| `subTotalPrice` | body | `number` | yes | Subtotal price |
| `salesTax` | body | `number` | yes | Sales tax amount |
| `totalPrice` | body | `number` | yes | Total price |
| `dueDate` | body | `date` | yes | Invoice due date |
| `currency` | body | `string` | yes | Currency code |
| `invoiceNo` | body | `string` | yes | Invoice number |
| `project.key` | body | `string` | no | Project ID |
| `name` | body | `string` | no | Invoice name |
