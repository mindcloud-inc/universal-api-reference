# Delete Contact List with Selzy

Deletes an existing contact list from Selzy.

## Endpoint

- **Method:** `POST`
- **Path:** `deleteList`
- **Base URL:** `https://api.selzy.com/en/api`
- **Official documentation:** [Delete Contact List](https://selzy.com/en/support/api/contacts/deletelist/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `list_id` | query | `number` | yes | List code from getLists or createList. |
