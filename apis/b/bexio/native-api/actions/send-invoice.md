# Send Invoice with Bexio

Sends an invoice from Bexio by email.

## Endpoint

- **Method:** `POST`
- **Path:** `/2.0/kb_invoice/:invoice_id/send`
- **Base URL:** `https://api.bexio.com`
- **Official documentation:** [Send Invoice](https://docs.bexio.com/#tag/Invoices/operation/v2SendInvoice)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `invoice_id` | path | `number` | yes | The ID of the invoice. |
| `recipient_email` | body | `string` | yes | During the trial period, the recipient is limited to the email address associated to the access token provided. |
| `subject` | body | `string` | yes | The email subject. |
| `message` | body | `string` | yes | The email message. The placeholder [Network Link] must be part of the text. |
| `mark_as_open` | body | `boolean` | no | Mark the invoice as open when sending the email. |
| `attach_pdf` | body | `boolean` | no | Attach the PDF directly to the email. |
