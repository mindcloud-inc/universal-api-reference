# Reply Ticket with Intercom

## Endpoint

- **Method:** `POST`
- **Path:** `/tickets/:ticket_id/reply`
- **Base URL:** `https://api.intercom.io`
- **Official documentation:** [Reply Ticket](https://developers.intercom.com/docs/references/rest-api/api.intercom.io/tickets/replyticket)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ticket_id` | path | `string` | yes | Intercom ticket identifier |
| `admin_id` | body | `string` | yes | Admin sending the reply |
| `body` | body | `string` | yes | Reply content |
