# Create Draft Process Flow Item with NileDesk

Creates a draft process flow item in NileDesk.

## Endpoint

- **Method:** `POST`
- **Path:** `/CreateProcessDraftItem`
- **Base URL:** `https://app.niledesk.com/api/public`
- **Official documentation:** [Create Draft Process Flow Item](https://niledesk.com/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `form_fields` | body | `object` | no | Optional process form field values keyed by NileDesk field identifier. |
| `form_tables` | body | `object` | no | Optional embedded table payload keyed by collection name. |
| `template_id` | body | `string` | yes | The NileDesk process template to create a draft item in. |
