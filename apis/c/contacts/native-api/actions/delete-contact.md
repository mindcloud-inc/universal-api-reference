# Delete Contact with Contacts+

Deletes an existing contact from Contacts+.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/contacts.delete`
- **Base URL:** `https://api.contactsplus.com`
- **Official documentation:** [Delete Contact](https://www.contactsplus.com/developers/contacts-api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contactId` | body | `string` | yes | The contact ID to delete. |
| `etag` | body | `string` | yes | The current contact ETag. |
| `teamId` | body | `string` | no | Delete the contact from this team instead of personal contacts. |
