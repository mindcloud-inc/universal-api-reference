# Create Ticket with Request Tracker (RT)

Creates a new ticket in Request Tracker.

## Endpoint

- **Method:** `POST`
- **Path:** `ticket`
- **Base URL:** `https://try.requesttracker.io/sufongepl_57381/REST/2.0/`
- **Official documentation:** [Create Ticket](https://docs.bestpractical.com/rt/6.0.2/RT/REST2.html#Tickets)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `AdminCc` | body | `string` | no | Admin Cc email address or RT user name. |
| `Cc` | body | `string` | no | Cc email address or RT user name. |
| `Content` | body | `string` | no | Initial ticket content or description. |
| `ContentType` | body | `string` | no | Content type for the initial ticket content, for example text/plain or text/html. |
| `Owner` | body | `string` | no | Owner user ID or username for the ticket. |
| `Priority` | body | `number` | no | Initial RT ticket priority value. |
| `Queue` | body | `string` | yes | Queue name or ID for the new ticket. |
| `Requestor` | body | `string` | no | Requestor email address or RT user name. |
| `Status` | body | `string` | no | Initial RT ticket status. |
| `Subject` | body | `string` | yes | Subject line for the new ticket. |
