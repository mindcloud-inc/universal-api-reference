# Add Single Contact To List with UseINBOX

Adds a contact to a list in UseINBOX.

## Endpoint

- **Method:** `POST`
- **Path:** `/inbox/v1/contactlists/:id/add`
- **Base URL:** `https://useapi.useinbox.com`
- **Official documentation:** [Add Single Contact To List](https://reference.useinbox.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Contact list ID from INBOX. |
| `email` | body | `string` | yes | Email address to add to the contact list. |
| `customFields[].customFieldId` | body | `string` | no | Custom field ID for the contact. |
| `customFields[].value` | body | `string` | no | Custom field value for the contact. |
