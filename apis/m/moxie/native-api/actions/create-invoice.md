# Create Invoice with Moxie

Creates a new invoice in Moxie.

## Endpoint

- **Method:** `POST`
- **Path:** `/action/invoices/create`
- **Base URL:** `https://pod01.withmoxie.com/api/public`
- **Official documentation:** [Create Invoice](https://help.withmoxie.com/en/articles/8174518-create-invoice)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `clientName` | body | `string` | yes | Existing client name for the invoice. |
| `dueDate` | body | `date` | no | Invoice due date. |
| `templateName` | body | `string` | no | Invoice template name. |
| `invoiceNumber` | body | `string` | no | Custom invoice number. |
| `taxRate` | body | `number` | no | Invoice tax rate percentage. |
| `discountPercent` | body | `number` | no | Invoice discount percentage. |
| `paymentInstructions` | body | `string` | no | Payment instructions shown on the invoice. |
| `items` | body | `list<object>` | yes | List of invoice line items. |
| `sendTo` | body | `object` | no | Recipient object for sending the invoice. |
