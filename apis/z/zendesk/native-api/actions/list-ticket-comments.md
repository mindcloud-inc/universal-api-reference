# List Ticket Comments with Zendesk

Retrieves comments for a Zendesk ticket.

## Endpoint

- **Method:** `GET`
- **Path:** `/tickets/:ticket_id/comments.json`
- **Base URL:** `https://{subdomain}.zendesk.com/api/v2`
- **Official documentation:** [List Ticket Comments](https://developer.zendesk.com/api-reference/ticketing/tickets/ticket_comments/#list-comments)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ticket_id` | path | `number` | yes | Zendesk ticket ID. |
