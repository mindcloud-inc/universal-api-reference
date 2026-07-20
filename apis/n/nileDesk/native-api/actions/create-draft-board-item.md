# Create Draft Board Item with NileDesk

Creates a draft board item in NileDesk.

## Endpoint

- **Method:** `POST`
- **Path:** `/CreateBoardDraftItem`
- **Base URL:** `https://app.niledesk.com/api/public`
- **Official documentation:** [Create Draft Board Item](https://niledesk.com/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `form_fields` | body | `object` | no | Optional board form field values keyed by NileDesk field identifier. |
| `form_tables` | body | `object` | no | Optional embedded table payload keyed by collection name. |
| `template_id` | body | `string` | yes | The NileDesk board template to create a draft item in. |
