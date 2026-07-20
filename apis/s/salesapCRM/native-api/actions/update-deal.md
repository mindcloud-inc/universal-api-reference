# Update Deal with SalesapCRM

Updates a deal in SalesapCRM.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/deals/{id}`
- **Base URL:** `https://app.salesap.ru/api/v1`
- **Official documentation:** [Update Deal](https://api.salesap.ru/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | SalesapCRM deal record ID from the path. |
| `data` | body | `object` | yes | JSON:API data object for updating a deal, including type, attributes, and optional relationships. |
