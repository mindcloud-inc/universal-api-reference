# List Ticket Audits with Zendesk

Retrieves audits for a Zendesk ticket.

## Endpoint

- **Method:** `GET`
- **Path:** `/tickets/:ticket_id/audits.json`
- **Base URL:** `https://{subdomain}.zendesk.com/api/v2`
- **Official documentation:** [List Ticket Audits](https://developer.zendesk.com/api-reference/ticketing/tickets/ticket_audits/#list-audits-for-a-ticket)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ticket_id` | path | `number` | yes | Zendesk ticket ID. |
