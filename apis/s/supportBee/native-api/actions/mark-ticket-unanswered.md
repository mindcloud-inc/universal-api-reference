# Mark Ticket Unanswered with SupportBee

Marks a SupportBee ticket as unanswered.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/tickets/:id/answered`
- **Base URL:** `https://{company}.supportbee.com`
- **Official documentation:** [Mark Ticket Unanswered](https://supportbee.com/docs/api/reference#tag/Tickets/paths/~1tickets~1{id}~1answered/delete)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | SupportBee ticket ID. |
