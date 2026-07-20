# Add Label to Ticket with SupportBee

Adds a label to a SupportBee ticket.

## Endpoint

- **Method:** `POST`
- **Path:** `/tickets/:ticket_id/labels/:label_name`
- **Base URL:** `https://{company}.supportbee.com`
- **Official documentation:** [Add Label to Ticket](https://supportbee.com/docs/api/reference#tag/Labels/paths/~1tickets~1{ticket_id}~1labels~1{label_name}/post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ticket_id` | path | `number` | yes | SupportBee ticket ID. |
| `label_name` | path | `string` | yes | Label name to attach to the ticket. |
