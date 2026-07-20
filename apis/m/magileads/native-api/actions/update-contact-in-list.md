# Update Contact In List with Magileads

Updates a contact in a Magileads contact list.

## Endpoint

- **Method:** `PUT`
- **Path:** `/contact-lists/:contact_list_id/contacts/:contact_id`
- **Base URL:** `https://app.api-magileads.net`
- **Official documentation:** [Update Contact In List](https://api.magileads.net)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contact_list_id` | path | `number` | yes | The contact list ID. |
| `contact_id` | path | `number` | yes | The contact ID. |
| `properties[]` | body | `array<object>` | yes | The contact properties to update. |
