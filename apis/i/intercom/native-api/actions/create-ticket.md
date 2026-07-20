# Create Ticket with Intercom

## Endpoint

- **Method:** `POST`
- **Path:** `/tickets`
- **Base URL:** `https://api.intercom.io`
- **Official documentation:** [Create Ticket](https://developers.intercom.com/docs/references/rest-api/api.intercom.io/tickets/createticket)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ticket_type_id` | body | `string` | yes | Intercom ticket type identifier |
| `contacts[]` | body | `array` | no | — |
| `contacts[].id` | body | `string` | yes | Contact ID to associate with the ticket |
| `ticket_attributes` | body | `object` | no | — |
| `ticket_attributes._default_title_` | body | `string` | no | Default ticket title |
| `ticket_attributes._default_description_` | body | `string` | no | Default ticket description |
