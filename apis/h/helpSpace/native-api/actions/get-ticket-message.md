# Get Ticket Message with HelpSpace

Retrieves a ticket message from HelpSpace.

## Endpoint

- **Method:** `GET`
- **Path:** `/tickets/{ticket_id}/messages/{message_id}`
- **Base URL:** `https://api.helpspace.com/api/v1`
- **Official documentation:** [Get Ticket Message](https://documentation.helpspace.com/api-message)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `message_id` | path | `string` | yes | HelpSpace message identifier. |
| `ticket_id` | path | `string` | yes | HelpSpace ticket identifier. |
