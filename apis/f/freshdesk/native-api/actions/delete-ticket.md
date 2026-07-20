# Delete Ticket with Freshdesk

Deletes an existing ticket from Freshdesk.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/tickets/:id`
- **Base URL:** `https://{subdomain}.freshdesk.com/api/v2`
- **Official documentation:** [Delete Ticket](https://developers.freshdesk.com/api/#delete_a_ticket)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `list<number>` | yes | Freshdesk ticket ID. |
