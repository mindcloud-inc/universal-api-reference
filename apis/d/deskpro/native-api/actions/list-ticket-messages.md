# List Ticket Messages with Deskpro

Retrieves a list of ticket messages from Deskpro.

## Endpoint

- **Method:** `GET`
- **Path:** `/tickets/:ticketId/messages`
- **Base URL:** `{helpdeskUrl}/api/v2`
- **Official documentation:** [List Ticket Messages](https://www.deskpro.com/developers/api-docs/v2.html#get--api-v2-tickets-{parentId}-messages)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ticketId` | path | `number` | yes | The Deskpro ticket id whose messages to list. |
