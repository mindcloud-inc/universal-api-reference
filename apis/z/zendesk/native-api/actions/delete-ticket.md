# Delete Ticket with Zendesk

Deletes an existing ticket from Zendesk.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/tickets/:id.json`
- **Base URL:** `https://{subdomain}.zendesk.com/api/v2`
- **Official documentation:** [Delete Ticket](https://developer.zendesk.com/api-reference/ticketing/tickets/tickets/#delete-ticket)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Zendesk ticket ID. |
