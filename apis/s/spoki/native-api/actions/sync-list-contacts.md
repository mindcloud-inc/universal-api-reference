# Sync List Contacts with Spoki

Creates or updates up to 500 contacts and adds them to the selected list.

## Endpoint

- **Method:** `POST`
- **Path:** `/lists/{{id}}/sync_contacts/`
- **Base URL:** `https://api.spoki.com/api/1`
- **Official documentation:** [Sync List Contacts](https://documenter.getpostman.com/view/21611004/UzBqnPvF)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | The list ID. |
| `contacts[]` | body | `array<object>` | yes | Contacts to create or update and add to the list. |
