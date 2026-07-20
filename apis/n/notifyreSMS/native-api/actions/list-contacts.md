# List Contacts with Notifyre SMS

Finds contacts in Notifyre by search filters.

## Endpoint

- **Method:** `POST`
- **Path:** `/addressbook/contacts/search`
- **Base URL:** `https://api.notifyre.com/20220711`
- **Official documentation:** [List Contacts](https://docs.notifyre.com/api/address-book-contacts-list)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `groupIds` | body | `list<string>` | no | Restrict results to these groups. |
| `includeUnsubscribed` | body | `boolean` | no | Whether unsubscribed contacts should be included. |
| `limit` | body | `number` | no | Maximum contacts to return. |
| `page` | body | `number` | no | Page number for contacts listing. |
| `searchQuery` | body | `string` | no | Search term for contacts. |
| `sortBy` | body | `string` | no | Field used to sort contacts. |
| `sortDir` | body | `string` | no | Sort direction for contacts. |
| `type` | body | `string` | no | Contact type filter. |
