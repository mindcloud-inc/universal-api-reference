# Add Contacts To Groups with Notifyre SMS

Adds contacts to groups in Notifyre.

## Endpoint

- **Method:** `POST`
- **Path:** `/addressbook/groups/contacts`
- **Base URL:** `https://api.notifyre.com/20220711`
- **Official documentation:** [Add Contacts To Groups](https://docs.notifyre.com/api/address-book-contacts-add-to-groups)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contacts` | body | `list<string>` | yes | Contacts to add to groups. |
| `groups` | body | `list<string>` | yes | Target groups. |
