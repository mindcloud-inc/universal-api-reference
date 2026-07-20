# Create Ticket QR Data with Ticket Generator

Creates ticket QR code data and ticket ID in Ticket Generator.

## Endpoint

- **Method:** `POST`
- **Path:** `v1/ticket/data/`
- **Base URL:** `https://apis.ticket-generator.com/client`
- **Official documentation:** [Create Ticket QR Data](https://apis.ticket-generator.com/client/api-docs/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `eventId` | query | `string` | yes | Ticket Generator event identifier. |
| `ticketCategoryId` | query | `string` | no | Ticket category identifier. Optional when the event has exactly one ticket category. |
| `width` | query | `number` | yes | Generated ticket width in pixels. |
