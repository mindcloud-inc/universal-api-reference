# Create CRM Ticket with ChatDaddy

Creates a new CRM ticket in ChatDaddy.

## Endpoint

- **Method:** `POST`
- **Path:** `/crm/tickets`
- **Base URL:** `https://api.chatdaddy.tech/im`
- **Official documentation:** [Create CRM Ticket](https://chatdaddy.stoplight.io/docs/openapi/f662d3d411a76-create-a-new-crm-ticket)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `boardId` | body | `string` | yes | CRM board identifier for the ticket. |
| `contactId` | body | `string` | yes | Contact identifier to associate with the ticket. |
| `stageId` | body | `string` | no | Optional CRM stage identifier for the ticket. |
| `title` | body | `string` | yes | CRM ticket title. |
