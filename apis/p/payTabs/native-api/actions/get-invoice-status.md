# Get Invoice Status with PayTabs

## Endpoint

- **Method:** `POST`
- **Path:** `/payment/invoice/status`
- **Base URL:** `{apiBaseUrl}`
- **Official documentation:** [Get Invoice Status](https://docs.paytabs.com/manuals/PT-API-Endpoints/Integration-Types-Manuals/Invoices-APIs/Invoices-Step-7-Manage-Transactions/Invoices-Step-7-Invoice-status/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `invoice_id` | body | `string` | yes | Invoice identifier to inspect. |
