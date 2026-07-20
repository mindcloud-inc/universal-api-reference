# Update One Record with NileDesk

Updates a single record in NileDesk.

## Endpoint

- **Method:** `POST`
- **Path:** `/UpdateOneRecord`
- **Base URL:** `https://app.niledesk.com/api/public`
- **Official documentation:** [Update One Record](https://niledesk.com/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `fields` | body | `object` | yes | The field values to apply to the matching record. |
| `filters` | body | `object` | yes | The NileDesk filter object used to identify the record to update. |
| `template_id` | body | `string` | yes | The NileDesk template containing the record to update. |
