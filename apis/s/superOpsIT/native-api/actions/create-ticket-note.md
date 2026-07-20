# Create Ticket Note with SuperOps IT

## Endpoint

- **Method:** `POST`
- **Path:** `/it`
- **Base URL:** `https://api.superops.ai`
- **Official documentation:** [Create Ticket Note](https://developer.superops.com/it#mutation-createTicketNote)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ticketId` | body | `string` | yes | The SuperOps ticket ID. |
| `content` | body | `string` | yes | The note content. |
| `addedByUserId` | body | `string` | no | Optional technician user ID adding the note. |
| `addedOn` | body | `date` | no | Optional note creation time in ISO 8601 format. |
| `privacyType` | body | `string` | no | PUBLIC or PRIVATE. |
