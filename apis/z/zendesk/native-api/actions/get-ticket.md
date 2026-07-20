# Get Ticket with Zendesk

Retrieves a ticket from Zendesk.

## Endpoint

- **Method:** `GET`
- **Path:** `/tickets/:id.json`
- **Base URL:** `https://{subdomain}.zendesk.com/api/v2`
- **Official documentation:** [Get Ticket](https://developer.zendesk.com/api-reference/ticketing/tickets/tickets/#show-ticket)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Zendesk ticket ID. |
