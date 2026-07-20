# Update Ticket with SuperOps IT

## Endpoint

- **Method:** `POST`
- **Path:** `/it`
- **Base URL:** `https://api.superops.ai`
- **Official documentation:** [Update Ticket](https://developer.superops.com/it#mutation-updateTicket)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ticketId` | body | `string` | yes | The SuperOps ticket ID to update. |
| `subject` | body | `string` | no | Optional new ticket subject. |
| `status` | body | `string` | no | Optional ticket status name. |
| `priority` | body | `string` | no | Optional ticket priority name. |
| `resolutionCode` | body | `string` | no | Optional ticket resolution code. |
| `requestType` | body | `string` | no | Optional ticket request type name. |
| `requesterUserId` | body | `string` | no | Optional requester user ID. |
| `technicianUserId` | body | `string` | no | Optional technician user ID. |
