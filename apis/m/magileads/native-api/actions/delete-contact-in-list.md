# Delete Contact In List with Magileads

Deletes a contact from a Magileads contact list.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/contact-lists/:contact_list_id/contacts/:contact_id`
- **Base URL:** `https://app.api-magileads.net`
- **Official documentation:** [Delete Contact In List](https://api.magileads.net)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contact_list_id` | path | `number` | yes | The contact list ID. |
| `contact_id` | path | `number` | yes | The contact ID. |
