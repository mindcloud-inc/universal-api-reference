# Create Comment on Ticket with Moxie

Creates a comment on a ticket in Moxie.

## Endpoint

- **Method:** `POST`
- **Path:** `/action/tickets/comments/create`
- **Base URL:** `https://pod01.withmoxie.com/api/public`
- **Official documentation:** [Create Comment on Ticket](https://help.withmoxie.com/en/articles/9367926-create-comment-on-ticket)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `userEmail` | body | `string` | yes | Email of the user posting the comment. |
| `ticketNumber` | body | `number` | yes | Numeric ticket number. |
| `privateComment` | body | `boolean` | yes | Whether the comment is private. |
| `comment` | body | `string` | yes | Comment body. |
