# Add Ticket Labels with GrooveHQ

Adds labels to a ticket in GrooveHQ.

## Endpoint

- **Method:** `POST`
- **Path:** `/tickets/:ticketNumber/tags`
- **Base URL:** `https://api.groovehq.com/v1`
- **Official documentation:** [Add Ticket Labels](https://doc.groovehq.com/tickets)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ticketNumber` | path | `string` | yes | — |
| `tags[]` | body | `array<string>` | yes | Send multiple values as a array. |
