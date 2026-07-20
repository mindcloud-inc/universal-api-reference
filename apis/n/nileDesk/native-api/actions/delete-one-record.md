# Delete One Record with NileDesk

Deletes a single record from NileDesk.

## Endpoint

- **Method:** `POST`
- **Path:** `/DeleteOneRecord`
- **Base URL:** `https://app.niledesk.com/api/public`
- **Official documentation:** [Delete One Record](https://niledesk.com/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filters` | body | `object` | yes | The NileDesk filter object used to identify the record to delete. |
| `template_id` | body | `string` | yes | The NileDesk template containing the record to delete. |
