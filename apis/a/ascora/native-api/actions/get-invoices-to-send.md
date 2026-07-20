# Get Invoices To Send with Ascora

Retrieves customer invoices ready to send from Ascora.

## Endpoint

- **Method:** `GET`
- **Path:** `/Accounting/GetInvoicesToSend`
- **Base URL:** `https://api.ascora.com.au`
- **Official documentation:** [Get Invoices To Send](https://www.dropbox.com/scl/fi/75586ygs35arfb7d3cvxi/API-Endpoints-1.2.pdf?rlkey=ztci7pf4nuasegnybjreqsqe2&dl=0#page=71)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `includeCustomerCustomFields` | query | `boolean` | no | Set to true to include custom fields for the related Billing Customer. |
| `includeInvoiceCustomFields` | query | `boolean` | no | Set to true to include custom fields for the related Invoice. |
| `includeJobCustomFields` | query | `boolean` | no | Set to true to include custom fields for the related Job. |
| `priorToDate` | query | `date` | yes | Only invoices that are dated prior to this date will be included. |
