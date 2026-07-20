# Send Process Item Forward with NileDesk

Sends a process item forward in NileDesk.

## Endpoint

- **Method:** `POST`
- **Path:** `/ProcessItem`
- **Base URL:** `https://app.niledesk.com/api/public`
- **Official documentation:** [Send Process Item Forward](https://niledesk.com/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `form_fields` | body | `object` | no | Optional process form field values keyed by NileDesk field identifier. |
| `form_tables` | body | `object` | no | Optional embedded table payload keyed by collection name. |
| `process_id` | body | `string` | yes | The NileDesk process item to move forward. |
| `remarks` | body | `string` | no | Optional remarks to store with the transition. |
| `step_id` | body | `string` | yes | The NileDesk step identifier the item should process from. |
