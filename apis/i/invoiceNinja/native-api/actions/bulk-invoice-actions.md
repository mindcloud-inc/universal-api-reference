# Bulk Invoice Actions with Invoice Ninja

## Endpoint

- **Method:** `POST`
- **Path:** `/invoices/bulk`
- **Base URL:** `https://invoicing.co/api/v1`
- **Official documentation:** [Bulk Invoice Actions](https://api-docs.invoicing.co/#tag/invoices/operation/bulkInvoices)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `action` | body | `string` | yes | Bulk action such as mark_sent, archive, delete, or email. |
| `ids` | body | `list<string>` | yes | Array of invoice ids to act on. |
| `email_type` | body | `string` | no | Email template type when emailing invoices. |
