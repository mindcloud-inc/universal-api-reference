# Update Ticket Properties with HappyFox

Updates ticket properties in HappyFox.

## Endpoint

- **Method:** `POST`
- **Path:** `/ticket/:ticket_number/staff_update/`
- **Base URL:** `https://{accountDomain}/api/1.1/json`
- **Official documentation:** [Update Ticket Properties](https://support.happyfox.com/kb/article/1039-tickets-endpoint/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ticket_number` | path | `string` | yes | HappyFox ticket number from the ticket display ID without the prefix. |
| `staff` | body | `number` | yes | — |
| `priority` | body | `number` | no | HappyFox priority ID for the ticket. |
| `assignee` | body | `number` | no | Optional HappyFox staff user ID to assign the ticket to. |
| `status` | body | `number` | no | Optional HappyFox status ID for the ticket. |
