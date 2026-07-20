# Create Ticket with SuperOps IT

## Endpoint

- **Method:** `POST`
- **Path:** `/it`
- **Base URL:** `https://api.superops.ai`
- **Official documentation:** [Create Ticket](https://developer.superops.com/it#mutation-createTicket)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `subject` | body | `string` | yes | The subject of the ticket. |
| `description` | body | `string` | no | The description of the ticket. |
| `siteId` | body | `string` | yes | The site ID associated with the ticket. |
| `requestType` | body | `string` | yes | The ticket request type name. |
| `requesterUserId` | body | `string` | no | Optional requester user ID. |
| `technicianUserId` | body | `string` | no | Optional technician user ID. |
| `status` | body | `string` | no | Optional ticket status name. |
| `priority` | body | `string` | no | Optional ticket priority name. |
