# Update Contact List with UseINBOX

Updates an existing contact list in UseINBOX.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/inbox/v1/contactlists/:id`
- **Base URL:** `https://useapi.useinbox.com`
- **Official documentation:** [Update Contact List](https://reference.useinbox.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Contact list ID from INBOX. |
| `listName` | body | `string` | no | Updated contact list name. |
