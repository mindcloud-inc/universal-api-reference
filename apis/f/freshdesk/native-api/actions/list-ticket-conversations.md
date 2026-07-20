# List Ticket Conversations with Freshdesk

Retrieves ticket conversations from Freshdesk by ticket ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/tickets/:id/conversations`
- **Base URL:** `https://{subdomain}.freshdesk.com/api/v2`
- **Official documentation:** [List Ticket Conversations](https://developers.freshdesk.com/api/#list_all_ticket_notes)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `list<number>` | yes | Freshdesk ticket ID. |
