# Delete Contacts with Notifyre SMS

Deletes selected contacts from Notifyre address book.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/addressbook/contacts`
- **Base URL:** `https://api.notifyre.com/20220711`
- **Official documentation:** [Delete Contacts](https://docs.notifyre.com/api/address-book-contacts-delete)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contacts` | body | `list<string>` | yes | Contacts to delete. |
