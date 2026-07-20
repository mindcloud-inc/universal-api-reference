# Update Contact with SalesapCRM

Updates a contact in SalesapCRM.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/contacts/{id}`
- **Base URL:** `https://app.salesap.ru/api/v1`
- **Official documentation:** [Update Contact](https://api.salesap.ru/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | SalesapCRM contact record ID from the path. |
| `data` | body | `object` | yes | JSON:API data object for updating a contact, including type, attributes, and optional relationships. |
