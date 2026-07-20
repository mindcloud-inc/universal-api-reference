# List Ticket Time Entries with Freshdesk

Retrieves time entries for a Freshdesk ticket.

## Endpoint

- **Method:** `GET`
- **Path:** `/tickets/:id/time_entries`
- **Base URL:** `https://{subdomain}.freshdesk.com/api/v2`
- **Official documentation:** [List Ticket Time Entries](https://developers.freshdesk.com/api/#list_all_ticket_timeentries)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `list<number>` | yes | Freshdesk ticket ID. |
