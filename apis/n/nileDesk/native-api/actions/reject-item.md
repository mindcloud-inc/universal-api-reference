# Reject Item with NileDesk

Rejects a process item in NileDesk.

## Endpoint

- **Method:** `POST`
- **Path:** `/RejectItem`
- **Base URL:** `https://app.niledesk.com/api/public`
- **Official documentation:** [Reject Item](https://niledesk.com/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `form_fields` | body | `object` | no | Optional process form field values keyed by NileDesk field identifier. |
| `form_tables` | body | `object` | no | Optional embedded table payload keyed by collection name. |
| `process_id` | body | `string` | yes | The NileDesk process item to reject. |
| `remarks` | body | `string` | no | Optional remarks to store with the rejection. |
| `step_id` | body | `string` | no | Optional NileDesk step identifier when rejection is step-scoped. |
