# Add ticket comment with Atera

Creates a comment on a specific Atera ticket.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v3/tickets/:ticketId/comments`
- **Base URL:** `https://app.atera.com`
- **Official documentation:** [Add ticket comment](https://app.atera.com/apidocs#!/Ticket/Ticket_AddCommentToTicketAsync)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `CommentTimestampUTC` | body | `string` | no | UTC comment timestamp. |
| `EnduserCommentDetails.EnduserId` | body | `number` | no | End user ID for end user comments. |
| `TechnicianCommentDetails.IsInternal` | body | `boolean` | no | Whether the technician comment is internal. |
| `TechnicianCommentDetails.TechnicianEmail` | body | `string` | no | Technician email for technician comments. |
| `TechnicianCommentDetails.TechnicianId` | body | `number` | no | Technician ID for technician comments. |
| `ticketId` | path | `number` | yes | System ticket ID. |
| `CommentText` | body | `string` | yes | Comment text. |
