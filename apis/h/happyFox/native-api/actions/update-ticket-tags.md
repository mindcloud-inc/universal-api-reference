# Update Ticket Tags with HappyFox

Updates a ticket's tags in HappyFox.

## Endpoint

- **Method:** `POST`
- **Path:** `/ticket/:ticket_number/update_tags/`
- **Base URL:** `https://{accountDomain}/api/1.1/json`
- **Official documentation:** [Update Ticket Tags](https://support.happyfox.com/kb/article/1039-tickets-endpoint/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ticket_number` | path | `string` | yes | HappyFox ticket number from the ticket display ID without the prefix. |
| `staff_id` | body | `number` | yes | — |
| `add` | body | `string` | no | Comma-separated ticket tags. |
| `remove` | body | `string` | no | — |
