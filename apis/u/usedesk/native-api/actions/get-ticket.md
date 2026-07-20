# Get Ticket with Usedesk

Retrieves a ticket by ID from Usedesk.

## Endpoint

- **Method:** `POST`
- **Path:** `/ticket`
- **Base URL:** `https://secure.usedesk.com/uapi`
- **Official documentation:** [Get Ticket](https://api.usedocs.com/article/51377)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ticket_id` | body | `number` | yes | Ticket ID. |
| `accessible_for_agent_id` | body | `number` | no | Agent ID used to evaluate access rights for the ticket. |
| `properties[]` | body | `array<string>` | no | Additional ticket properties to include, such as SLA values. |
