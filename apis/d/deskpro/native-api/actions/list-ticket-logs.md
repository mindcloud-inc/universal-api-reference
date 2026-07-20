# List Ticket Logs with Deskpro

Retrieves a list of ticket logs from Deskpro.

## Endpoint

- **Method:** `GET`
- **Path:** `/tickets/:ticketId/logs`
- **Base URL:** `{helpdeskUrl}/api/v2`
- **Official documentation:** [List Ticket Logs](https://www.deskpro.com/developers/api-docs/v2.html#get--api-v2-tickets-{parentId}-logs)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ticketId` | path | `number` | yes | The Deskpro ticket id whose logs to list. |
