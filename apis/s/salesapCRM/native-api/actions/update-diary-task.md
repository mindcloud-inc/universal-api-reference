# Update Diary Task with SalesapCRM

Updates a diary task in SalesapCRM.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/diary-tasks/{id}`
- **Base URL:** `https://app.salesap.ru/api/v1`
- **Official documentation:** [Update Diary Task](https://api.salesap.ru/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | SalesapCRM diary task record ID from the path. |
| `data` | body | `object` | yes | JSON:API data object for updating a diary task, including type, attributes, and optional relationships. |
