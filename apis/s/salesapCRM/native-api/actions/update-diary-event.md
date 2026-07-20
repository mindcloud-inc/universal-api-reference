# Update Diary Event with SalesapCRM

Updates a diary event in SalesapCRM.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/diary-events/{id}`
- **Base URL:** `https://app.salesap.ru/api/v1`
- **Official documentation:** [Update Diary Event](https://api.salesap.ru/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | SalesapCRM diary event record ID from the path. |
| `data` | body | `object` | yes | JSON:API data object for updating a diary event, including type, attributes, and optional relationships. |
