# Update Invoice with SalesapCRM

Updates an invoice in SalesapCRM.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/invoices/{id}`
- **Base URL:** `https://app.salesap.ru/api/v1`
- **Official documentation:** [Update Invoice](https://api.salesap.ru/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | SalesapCRM invoice record ID from the path. |
| `data` | body | `object` | yes | JSON:API data object for updating an invoice, including type, attributes, and optional relationships. |
