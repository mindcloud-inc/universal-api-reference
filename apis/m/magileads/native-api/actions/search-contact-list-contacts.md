# Search Contact List Contacts with Magileads

Finds contacts in a Magileads contact list by criteria.

## Endpoint

- **Method:** `POST`
- **Path:** `/contact-lists/:contact_list_id/contacts/search`
- **Base URL:** `https://app.api-magileads.net`
- **Official documentation:** [Search Contact List Contacts](https://api.magileads.net)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contact_list_id` | path | `number` | yes | The contact list ID. |
| `query` | body | `string` | yes | The text to search for in the contact list. |
