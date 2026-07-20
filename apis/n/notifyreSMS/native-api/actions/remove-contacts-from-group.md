# Remove Contacts From Group with Notifyre SMS

Removes contacts from a Notifyre group.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/addressbook/groups/contacts`
- **Base URL:** `https://api.notifyre.com/20220711`
- **Official documentation:** [Remove Contacts From Group](https://docs.notifyre.com/api/address-book-contacts-remove-from-group)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contacts` | body | `list<string>` | yes | Contacts to remove from the group. |
| `groupID` | body | `string` | yes | Group identifier for removal. |
