# Cancel Invoice with PayTabs

## Endpoint

- **Method:** `POST`
- **Path:** `/payment/invoice/cancel`
- **Base URL:** `{apiBaseUrl}`
- **Official documentation:** [Cancel Invoice](https://docs.paytabs.com/manuals/PT-API-Endpoints/Integration-Types-Manuals/Invoices-APIs/Invoices-Step-7-Manage-Transactions/Invoices-Step-7-Cancel-Invoice/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `invoice_id` | body | `string` | yes | Invoice identifier to cancel. |
