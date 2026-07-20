# List Contacts by ID with Contacts+

Retrieves contacts from Contacts+ by ID.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/contacts.get`
- **Base URL:** `https://api.contactsplus.com`
- **Official documentation:** [List Contacts by ID](https://www.contactsplus.com/developers/contacts-api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contactIds[]` | body | `array<string>` | yes | The contact IDs to retrieve. |
| `teamId` | body | `string` | no | Retrieve contacts from this team instead of personal contacts. |
