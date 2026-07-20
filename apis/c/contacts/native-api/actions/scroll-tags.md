# Scroll Tags with Contacts+

Retrieves tags from Contacts+ using a scroll cursor.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/tags.scroll`
- **Base URL:** `https://api.contactsplus.com`
- **Official documentation:** [Scroll Tags](https://www.contactsplus.com/developers/contacts-api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `size` | body | `number` | no | Maximum number of tags to return. |
| `scrollCursor` | body | `string` | no | Cursor for the next page of tags. Leave blank for the first page. |
