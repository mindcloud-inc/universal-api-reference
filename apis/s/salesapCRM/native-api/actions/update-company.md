# Update Company with SalesapCRM

Updates a company in SalesapCRM.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/companies/{id}`
- **Base URL:** `https://app.salesap.ru/api/v1`
- **Official documentation:** [Update Company](https://api.salesap.ru/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | SalesapCRM company record ID from the path. |
| `data` | body | `object` | yes | JSON:API data object for updating a company, including type, attributes, and optional relationships. |
