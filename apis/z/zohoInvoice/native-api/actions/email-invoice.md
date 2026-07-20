# Email Invoice with Zoho Invoice

Emails an invoice from Zoho Invoice.

## Endpoint

- **Method:** `POST`
- **Path:** `/invoices/:invoice_id/email`
- **Base URL:** `https://www.zohoapis.com/invoice/v3`
- **Official documentation:** [Email Invoice](https://www.zoho.com/invoice/api/v3/invoices/#email-an-invoice)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organization_id` | query | `list<string>` | yes | ID of the organization header X-com-zoho-invoice-organizationid. |
| `invoice_id` | path | `string` | yes | Unique identifier of the invoice. |
| `send_from_org_email_id` | body | `boolean` | no | Boolean to trigger the email from the organization's email address. |
| `to_mail_ids[]` | body | `array<string>` | yes | Array of email addresses of the recipients. |
| `cc_mail_ids[]` | body | `array<string>` | no | Array of email addresses of the recipients to be CC'd. |
| `subject` | body | `string` | no | The subject of the mail. |
| `body` | body | `string` | no | The body content of the mail. |
| `send_customer_statement` | query | `boolean` | no | Send customer statement PDF with the email. |
| `send_attachment` | query | `boolean` | no | Send the invoice attachment with the email. |
