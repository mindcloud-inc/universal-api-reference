# Scroll Contacts with Contacts+

Retrieves contacts from Contacts+ using a scroll cursor.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/contacts.scroll`
- **Base URL:** `https://api.contactsplus.com`
- **Official documentation:** [Scroll Contacts](https://www.contactsplus.com/developers/contacts-api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `size` | body | `number` | no | Maximum number of contacts to return. |
| `scrollCursor` | body | `string` | no | Cursor for the next page of contacts. Leave blank for the first page. |
