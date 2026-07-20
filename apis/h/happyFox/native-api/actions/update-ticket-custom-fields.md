# Update Ticket Custom Fields with HappyFox

Updates a ticket's custom fields in HappyFox.

## Endpoint

- **Method:** `POST`
- **Path:** `/ticket/:ticket_number/update_custom_fields/`
- **Base URL:** `https://{accountDomain}/api/1.1/json`
- **Official documentation:** [Update Ticket Custom Fields](https://support.happyfox.com/kb/article/1039-tickets-endpoint/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ticket_number` | path | `string` | yes | HappyFox ticket number from the ticket display ID without the prefix. |
| `staff` | body | `number` | yes | — |
