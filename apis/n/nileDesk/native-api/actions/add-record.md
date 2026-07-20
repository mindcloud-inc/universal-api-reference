# Add Record with NileDesk

Creates a new record in NileDesk.

## Endpoint

- **Method:** `POST`
- **Path:** `/AddRecord`
- **Base URL:** `https://app.niledesk.com/api/public`
- **Official documentation:** [Add Record](https://niledesk.com/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `fields` | body | `object` | yes | The record field values to insert. |
| `form_tables` | body | `object` | no | Optional embedded table payload keyed by collection name. |
| `template_id` | body | `string` | yes | The NileDesk dataset or form template to create the record in. |
