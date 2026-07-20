# List Emails with Google Mail

Retrieves messages from a Gmail mailbox.

## Endpoint

- **Method:** `GET`
- **Path:** `/messages`
- **Base URL:** `https://gmail.googleapis.com/gmail/v1/users/:userId`
- **Official documentation:** [List Emails](https://developers.google.com/workspace/gmail/api/reference/rest/v1/users.messages/list)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `q` | query | `string` | no | Search threads matching a query. Supports the same query format as the Gmail search box. For example: "from:myusername@example.com is:unread". |
| `labelIds` | query | `list<string>` | no | Only return messages with labels that match all of the specified label IDs. Messages in a thread might have labels that other messages in the same thread don't have. |
| `receivedAfter` | query | `date` | no | Filters emails to only include those received after a specified date and time |
