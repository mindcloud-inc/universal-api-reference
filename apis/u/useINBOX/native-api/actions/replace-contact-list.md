# Replace Contact List with UseINBOX

Replaces an existing contact list in UseINBOX.

## Endpoint

- **Method:** `PUT`
- **Path:** `/inbox/v1/contactlists/:id`
- **Base URL:** `https://useapi.useinbox.com`
- **Official documentation:** [Replace Contact List](https://reference.useinbox.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Contact list ID from INBOX. |
| `listName` | body | `string` | yes | Contact list name. |
| `groupId` | body | `string` | yes | Group ID for the contact list. |
| `legislation` | body | `number` | yes | INBOX legislation value for the contact list. |
