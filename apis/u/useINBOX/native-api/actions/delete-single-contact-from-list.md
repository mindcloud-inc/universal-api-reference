# Delete Single Contact From List with UseINBOX

Deletes a contact from a list in UseINBOX.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/inbox/v1/contactlists/:id/delete/:contact-id`
- **Base URL:** `https://useapi.useinbox.com`
- **Official documentation:** [Delete Single Contact From List](https://reference.useinbox.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Contact list ID from INBOX. |
| `contact-id` | path | `string` | yes | Contact ID to remove from the list. |
