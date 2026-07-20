# Search Invoices with PayTabs

## Endpoint

- **Method:** `POST`
- **Path:** `/payment/invoice/search`
- **Base URL:** `{apiBaseUrl}`
- **Official documentation:** [Search Invoices](https://docs.paytabs.com/manuals/PT-API-Endpoints/Integration-Types-Manuals/Invoices-APIs/Invoices-Step-7-Manage-Transactions/Invoices-Step-7-Search-Invoices-List/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `created_date_from` | body | `string` | yes | Lower bound creation date in the PayTabs search format. |
| `created_date_to` | body | `string` | yes | Upper bound creation date in the PayTabs search format. |
