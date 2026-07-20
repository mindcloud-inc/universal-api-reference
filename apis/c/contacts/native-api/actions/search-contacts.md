# Search Contacts with Contacts+

Finds contacts in Contacts+ by search query.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/contacts.search`
- **Base URL:** `https://api.contactsplus.com`
- **Official documentation:** [Search Contacts](https://www.contactsplus.com/developers/contacts-api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `searchQuery` | body | `string` | yes | Search text used to match contacts. |
| `searchCursor` | body | `string` | no | Cursor for the next page of search results. |
| `teamId` | body | `string` | no | Search contacts in this team instead of personal contacts. |
