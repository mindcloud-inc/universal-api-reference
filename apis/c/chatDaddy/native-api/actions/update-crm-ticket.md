# Update CRM Ticket with ChatDaddy

Updates an existing CRM ticket in ChatDaddy.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/crm/tickets/{id}`
- **Base URL:** `https://api.chatdaddy.tech/im`
- **Official documentation:** [Update CRM Ticket](https://chatdaddy.stoplight.io/docs/openapi/9fa1268186138-update-a-crm-ticket)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | CRM ticket identifier to update. |
| `title` | body | `string` | no | Updated CRM ticket title. |
