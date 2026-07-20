# Update Contact with Contacts+

Updates an existing contact in Contacts+.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/contacts.update`
- **Base URL:** `https://api.contactsplus.com`
- **Official documentation:** [Update Contact](https://www.contactsplus.com/developers/contacts-api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contact` | body | `object` | yes | The contact object to update, including contactId and etag. |
| `resolveConflicts` | body | `boolean` | no | Resolve server conflicts during update. |
| `teamId` | body | `string` | no | Update the contact in this team instead of personal contacts. |
