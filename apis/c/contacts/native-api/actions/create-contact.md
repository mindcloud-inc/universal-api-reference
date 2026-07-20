# Create Contact with Contacts+

Creates a new contact in Contacts+.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/contacts.create`
- **Base URL:** `https://api.contactsplus.com`
- **Official documentation:** [Create Contact](https://www.contactsplus.com/developers/contacts-api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contact` | body | `object` | yes | The contact object to create. |
| `teamId` | body | `string` | no | Create the contact in this team instead of personal contacts. |
