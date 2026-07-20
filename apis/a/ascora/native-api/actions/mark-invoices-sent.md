# Mark Invoices Sent with Ascora

Marks invoices as sent in Ascora.

## Endpoint

- **Method:** `POST`
- **Path:** `/Accounting/MarkInvoicesAsSent`
- **Base URL:** `https://api.ascora.com.au`
- **Official documentation:** [Mark Invoices Sent](https://www.dropbox.com/scl/fi/75586ygs35arfb7d3cvxi/API-Endpoints-1.2.pdf?rlkey=ztci7pf4nuasegnybjreqsqe2&dl=0#page=75)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `InvoiceIds[]` | body | `string` | yes | Invoice IDs to mark as sent. |
