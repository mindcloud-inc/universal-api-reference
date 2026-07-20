# List Groups with Notifyre SMS

Retrieves contact groups from the Notifyre address book.

## Endpoint

- **Method:** `GET`
- **Path:** `/addressbook/groups`
- **Base URL:** `https://api.notifyre.com/20220711`
- **Official documentation:** [List Groups](https://docs.notifyre.com/api/address-book-groups-list)

## Capabilities

This operation supports [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `searchQuery` | query | `string` | no | Search term for groups. |
| `sortBy` | query | `string` | no | Field used to sort groups. |
| `sortDir` | query | `string` | no | Sort direction for groups. |
