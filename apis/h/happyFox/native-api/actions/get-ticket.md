# Get Ticket with HappyFox

Retrieves a ticket from HappyFox.

## Endpoint

- **Method:** `GET`
- **Path:** `/ticket/:ticket_number/`
- **Base URL:** `https://{accountDomain}/api/1.1/json`
- **Official documentation:** [Get Ticket](https://support.happyfox.com/kb/article/1039-tickets-endpoint/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ticket_number` | path | `string` | yes | HappyFox ticket number from the ticket display ID without the prefix. |
