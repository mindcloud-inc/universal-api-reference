# Replace Ticket Labels with GrooveHQ

Replaces all labels on a ticket in GrooveHQ.

## Endpoint

- **Method:** `PUT`
- **Path:** `/tickets/:ticketNumber/tags`
- **Base URL:** `https://api.groovehq.com/v1`
- **Official documentation:** [Replace Ticket Labels](https://doc.groovehq.com/tickets)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ticketNumber` | path | `string` | yes | — |
| `tags[]` | body | `array<string>` | yes | Send multiple values as a array. |
