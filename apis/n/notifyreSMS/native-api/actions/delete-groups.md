# Delete Groups with Notifyre SMS

Deletes selected groups from Notifyre address book.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/addressbook/groups`
- **Base URL:** `https://api.notifyre.com/20220711`
- **Official documentation:** [Delete Groups](https://docs.notifyre.com/api/address-book-group-delete)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `groups` | body | `list<string>` | yes | Groups to delete. |
| `includeContacts` | body | `boolean` | yes | Whether contacts should also be removed. |
