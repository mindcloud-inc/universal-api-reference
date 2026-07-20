# Move Board Item To Step with NileDesk

Moves a board item to another step in NileDesk.

## Endpoint

- **Method:** `POST`
- **Path:** `/SwitchBoardStep`
- **Base URL:** `https://app.niledesk.com/api/public`
- **Official documentation:** [Move Board Item To Step](https://niledesk.com/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `board_drop_step` | body | `string` | yes | The target board step identifier. |
| `form_fields` | body | `object` | no | Optional board form field values keyed by NileDesk field identifier. |
| `form_tables` | body | `object` | no | Optional embedded table payload keyed by collection name. |
| `process_id` | body | `string` | yes | The NileDesk board item to move. |
