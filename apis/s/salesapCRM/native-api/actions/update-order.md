# Update Order with SalesapCRM

Updates an order in SalesapCRM.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/orders/{id}`
- **Base URL:** `https://app.salesap.ru/api/v1`
- **Official documentation:** [Update Order](https://api.salesap.ru/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | SalesapCRM order record ID from the path. |
| `data` | body | `object` | yes | JSON:API data object for updating an order, including type, attributes, and optional relationships. |
