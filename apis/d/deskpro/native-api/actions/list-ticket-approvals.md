# List Ticket Approvals with Deskpro

Retrieves a list of ticket approvals from Deskpro.

## Endpoint

- **Method:** `GET`
- **Path:** `/tickets/:ticketId/ticket_approvals`
- **Base URL:** `{helpdeskUrl}/api/v2`
- **Official documentation:** [List Ticket Approvals](https://www.deskpro.com/developers/api-docs/v2.html#get--api-v2-tickets-{ticketId}-ticket_approvals)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ticketId` | path | `number` | yes | The Deskpro ticket id whose approvals to list. |
