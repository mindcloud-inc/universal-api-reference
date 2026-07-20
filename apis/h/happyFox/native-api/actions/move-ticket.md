# Move Ticket with HappyFox

Moves a ticket to another category in HappyFox.

## Endpoint

- **Method:** `POST`
- **Path:** `/ticket/:ticket_number/move/`
- **Base URL:** `https://{accountDomain}/api/1.1/json`
- **Official documentation:** [Move Ticket](https://support.happyfox.com/kb/article/1039-tickets-endpoint/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ticket_number` | path | `string` | yes | HappyFox ticket number from the ticket display ID without the prefix. |
| `staff_id` | body | `number` | yes | — |
| `target_category_id` | body | `number` | yes | Destination HappyFox category ID. |
| `move_note` | body | `string` | no | — |
| `assign_to` | body | `number` | no | — |
