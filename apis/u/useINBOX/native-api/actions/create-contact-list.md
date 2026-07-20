# Create Contact List with UseINBOX

Creates a contact list in UseINBOX.

## Endpoint

- **Method:** `POST`
- **Path:** `/inbox/v1/contactlists`
- **Base URL:** `https://useapi.useinbox.com`
- **Official documentation:** [Create Contact List](https://reference.useinbox.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `listName` | body | `string` | yes | Contact list name. |
| `groupId` | body | `string` | yes | Group ID for the contact list. |
| `legislation` | body | `number` | yes | INBOX legislation value for the contact list. |
