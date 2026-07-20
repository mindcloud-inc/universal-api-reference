# Get Ticket Attachments with Request Tracker (RT)

Retrieves a ticket's attachments from Request Tracker.

## Endpoint

- **Method:** `GET`
- **Path:** `ticket/:ticketId/attachments`
- **Base URL:** `https://try.requesttracker.io/sufongepl_57381/REST/2.0/`
- **Official documentation:** [Get Ticket Attachments](https://docs.bestpractical.com/rt/6.0.2/RT/REST2.html#Attachments-and-Messages)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ticketId` | path | `string` | yes | The numeric RT ticket ID. |
