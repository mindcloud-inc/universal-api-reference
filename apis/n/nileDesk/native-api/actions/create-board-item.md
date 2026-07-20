# Create Board Item with NileDesk

Creates a live board item in NileDesk.

## Endpoint

- **Method:** `POST`
- **Path:** `/InitiateBoardItem`
- **Base URL:** `https://app.niledesk.com/api/public`
- **Official documentation:** [Create Board Item](https://niledesk.com/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `form_fields` | body | `object` | no | Optional board form field values keyed by NileDesk field identifier. |
| `form_tables` | body | `object` | no | Optional embedded table payload keyed by collection name. |
| `step_id` | body | `string` | yes | The target board drop step identifier. |
| `template_id` | body | `string` | yes | The NileDesk board template to initiate. |
